FROM mcr.microsoft.com/dotnet/sdk:6.0

WORKDIR /src
COPY . ./src

RUN dotnet build -o /app
RUN dotnet publish -o /publish

WORKDIR /publish
ENV ASPNETCORE_URLS=http://+:80/
EXPOSE 80

CMD ["./myWebApp"]