# use the node base image provided by official repo
FROM node:latest
MAINTAINER Steve Zhang "stevzhg@gmail.com"

# prepare work directory
WORKDIR /blog

# install hexo
RUN npm install hexo-cli -g
RUN npm install
RUN npm install hexo-generator-sitemap --save
RUN npm install hexo-generator-feed --save
RUN npm install hexo-deployer-git --save

# replace this with your application's default port
EXPOSE 4000

# run hexo server
CMD ["hexo", "server","-i","0.0.0.0"]