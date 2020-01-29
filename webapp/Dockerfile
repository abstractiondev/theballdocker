# Build runtime image
FROM abstractiondev/theballbase
WORKDIR /app
ADD https://tbpublicdeploy.file.core.windows.net/deploy/20200129.0631_dev_0588c104bbf9cd1267ccc569cd8284436bb71e36/WebApp.tar.gz?sv=2018-03-28&ss=bf&srt=co&sp=rl&se=2029-12-31T15:27:23Z&st=2019-01-28T07:27:23Z&spr=https&sig=fBVwNibZHKuhcN5r4RJlj9UB5R9mtShrapuXni2dY9M%3D ./
RUN tar xvfz ./WebApp.tar.gz
RUN mkdir /X
#RUN apt-get update && apt-get -y install cifs-utils
ENTRYPOINT ["dotnet", "WebCoreLayer.dll"]