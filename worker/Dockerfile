FROM mcr.microsoft.com/dotnet/sdk:2.1

WORKDIR /code

ADD worker/src/Worker /code/src/Worker

RUN dotnet restore -v minimal code/src/Worker \
    && dotnet publish -c Release -o "./" "code/src/Worker/" 

CMD dotnet code/src/Worker/Worker.dll
