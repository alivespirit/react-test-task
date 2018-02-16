FROM alpine:latest
RUN apk add --no-cache nodejs git && \
    git clone https://github.com/gothinkster/react-redux-realworld-example-app.git && \
    cd react-redux-realworld-example-app && \
    npm install && \ 
    sed -i "s.const API_ROOT.//const API_ROOT.g" src/agent.js && \
    sed -i "5i const API_ROOT = 'http://backend:3000/api';" src/agent.js

FROM alpine:latest
RUN apk add --no-cache nodejs
COPY --from=0 /react-redux-realworld-example-app /react-redux-realworld-example-app/
WORKDIR /react-redux-realworld-example-app
CMD [ "npm", "start" ]
EXPOSE 4100
