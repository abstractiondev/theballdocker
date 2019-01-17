# Build runtime image
FROM abstractiondev/theballbase
WORKDIR /app
ADD https://tbdevops.file.core.windows.net/deploy/20190117.0613_dev_7d365f91a6986b1e67c14e4ddaa1244f57362be8/WebApp.tar.gz?sv=2015-12-11&ss=f&srt=sco&sp=rl&se=2019-01-17T01:19:07Z&st=2017-01-16T17:19:07Z&spr=https&sig=vyaYn6ft2jTrGGC9hQ09FCGKDyzI35BUWVJjiOAsQTs%3D ./
RUN tar xvfz ./WebApp.tar.gz
RUN mkdir /X
#RUN apt-get update && apt-get -y install cifs-utils
ENTRYPOINT ["dotnet", "WebCoreLayer.dll"]