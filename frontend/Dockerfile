FROM node:20.12.1-bullseye-slim as build

WORKDIR /app

COPY frontend/package.json frontend/package-lock.json* ./
RUN npm install

COPY frontend/ ./
RUN npm run build

# 使用distroless镜像运行nginx以获得最小攻击面
FROM gcr.io/distroless/nginx:1.25.3
COPY --from=build /app/dist /usr/share/nginx/html
COPY frontend/nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80

# distroless镜像没有shell，因此使用直接命令方式
CMD ["nginx", "-g", "daemon off;"]
