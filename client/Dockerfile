FROM node:22
WORKDIR /client
# Clone the frontend repository
ARG FRONTEND_REPO_URL
RUN git clone $FRONTEND_REPO_URL app

WORKDIR /client/app
RUN npm install && npm run build

CMD ["npm", "run", "preview"]

