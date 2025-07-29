FROM node:14-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

# the rest of the files are copied after the dependencies are installed for efficiency as docker caches the files and does not reinstall dependencies
# it is reinstalled only if the package.json and not for each change in the source code(rest of the *.js, *.css, etc.)
COPY . .

EXPOSE 8080

CMD ["npm", "start"]