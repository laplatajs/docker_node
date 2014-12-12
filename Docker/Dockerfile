FROM dockerfile/nodejs
MAINTAINER Aldo Vizcaino <aldo.vizcaino87@gmail.com>

# Set correct environment variables.
ENV HOME /root
RUN apt-get -qqy install git
RUN git clone https://github.com/buritica/dibujemos.git /opt/dibujemos
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

WORKDIR /opt/dibujemos

RUN npm install express --save
RUN npm install socket.io --save
RUN npm install stylus --save
RUN npm install ejs --save

EXPOSE  3000
CMD ["node", "/opt/dibujemos/app.js"]
