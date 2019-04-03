
FROM microsoft/dotnet:sdk as build-env
WORKDIR /app

COPY *.csproj ./
RUN dotnet restore

COPY . ./
RUN	dotnet publish -c Release -o bin


FROM microsoft/dotnet:aspnetcore-runtime
#ARG source
WORKDIR /app
EXPOSE 80
COPY --from=build-env /app/bin
ENTRYPOINT ["dotnet", "CoreWeb.dll"]
