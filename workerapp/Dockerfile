# Build runtime image
FROM abstractiondev/theballbase
WORKDIR /app
ADD https://tbpublicdeploy.file.core.windows.net/deploy/20190323.1831_dev_94f9debac29f43f2a401314ecf6dea1363714a6d/WorkerApp.tar.gz?sv=2018-03-28&ss=bf&srt=co&sp=rl&se=2029-12-31T15:27:23Z&st=2019-01-28T07:27:23Z&spr=https&sig=fBVwNibZHKuhcN5r4RJlj9UB5R9mtShrapuXni2dY9M%3D ./
RUN tar xvfz ./WorkerApp.tar.gz
RUN mkdir /X
#RUN apt-get update && apt-get -y install cifs-utils
ENTRYPOINT ["dotnet", "TheBallWorkerConsole.dll"]