FROM node:18
WORKDIR /app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm install

COPY . .
RUN npm run build

CMD ["cp", "-r", "/app/build/.", "/frontend_static/"]