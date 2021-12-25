FROM node:16-alpine
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
CMD npm run build

FROM nginx
COPY --from=builder /app/build /user/share/nginx/html
