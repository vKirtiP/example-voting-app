FROM microsoft/dotnet:1.1.1-sdk

WORKDIR /code

ADD src/Worker /code/src/Worker

RUN dotnet restore -v minimal src/Worker \
	&& dotnet publish -c Relase -o "./" "src/Worker"

CMD dotnet /src/Worker/Worker.dll

