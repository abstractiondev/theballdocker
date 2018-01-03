# Build runtime image
FROM abstractiondev/theballbase
WORKDIR /app
ADD https://tbdevops.file.core.windows.net/deploy/20180103.1841_dev_a3af5d3a1fe62f80f39379ec95db2f4084186bba/WorkerApp.tar.gz?sv=2015-12-11&ss=f&srt=sco&sp=rl&se=2019-01-17T01:19:07Z&st=2017-01-16T17:19:07Z&spr=https&sig=vyaYn6ft2jTrGGC9hQ09FCGKDyzI35BUWVJjiOAsQTs%3D ./
RUN tar xvfz ./WorkerApp.tar.gz
RUN mkdir /X
#RUN apt-get update && apt-get -y install cifs-utils
ENTRYPOINT ["dotnet", "TheBallWorkerConsole.dll"]