FROM node:22
WORKDIR /server
# Clone the backend repository
ARG BACKEND_REPO_URL
RUN git clone $BACKEND_REPO_URL app

WORKDIR /server/app
RUN npm install && npm run set-env-prod && npm run  pri:generate && npm run  build 

CMD ["npm", "run", "start:prod"]

