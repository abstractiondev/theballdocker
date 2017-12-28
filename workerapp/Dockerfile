# Build runtime image
FROM microsoft/aspnetcore:2.0
WORKDIR /app
ADD https://tbdevops.file.core.windows.net/deploy/20171222.1438_dev_319586774f18c90a0da977026a670bbe3dc15b01/WorkerApp.tar.gz?sv=2015-12-11&ss=f&srt=sco&sp=rl&se=2019-01-17T01:19:07Z&st=2017-01-16T17:19:07Z&spr=https&sig=vyaYn6ft2jTrGGC9hQ09FCGKDyzI35BUWVJjiOAsQTs%3D ./
RUN tar xvfz ./WorkerApp.tar.gz
RUN mkdir /X
RUN apt-get update && apt-get -y install cifs-utils
ENTRYPOINT ["dotnet", "TheBallWorkerConsole.dll"]