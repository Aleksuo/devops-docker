FROM node

COPY . .
RUN npm install
RUN npm update caniuse-lite browserslist
CMD FRONT_URL=http://localhost:5000 npm start