#FROM microsoft/dotnet2.1-aspnetcore-runtime
#WORKDIR /app
#COPY ./out .
#ENTRYPOINT ["dotnet", "CoreWeb.dll"]


FROM microsoft/aspnetcore:2.0
ARG source
WORKDIR /app
EXPOSE 80
COPY ./out .
ENTRYPOINT ["dotnet", "CoreWeb.dll"]
