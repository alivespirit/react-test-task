# react-test-task
Frontend: [react-redux-realworld-example-app](https://github.com/gothinkster/react-redux-realworld-example-app)  
Backend: [rails-realworld-example-app](https://github.com/gothinkster/rails-realworld-example-app)  
  
Known issues:  
- frontend app can't connect to backend directly (on backend:3000) so need to change value in frontend [Dockerfile](react-redux-realworld-example-app/Dockerfile#L7) to host IP before running docker-compose. If fixed then [port 3000](docker-compose.yml#L10) can be closed.
