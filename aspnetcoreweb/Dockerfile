FROM microsoft/aspnetcore:1.1.1

# install nodejs for angular
RUN apt-get update
RUN apt-get -f install
RUN apt-get install -y wget
RUN wget -qO- https://deb.nodesource.com/setup_6.x | bash -
RUN apt-get install -y build-essential nodejs

WORKDIR /app
ENV ASPNETCORE_ENVIRONMENT Production
COPY published ./
ENTRYPOINT ["dotnet", "aspnetcoreweb.dll"]