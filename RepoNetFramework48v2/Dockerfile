# Usa la imagen de Windows Server Core con ASP.NET
FROM mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2019

# Establece el directorio de trabajo
WORKDIR /inetpub/wwwroot

# Copia todos los archivos de la aplicación al contenedor
COPY . .


# Expone el puerto 80
EXPOSE 80

# Establece el ENTRYPOINT para ejecutar IIS
ENTRYPOINT ["C:\\ServiceMonitor.exe", "w3svc"]


#repo-netframework-image