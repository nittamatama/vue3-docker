FROM node:16.13.2-alpine
WORKDIR /app
# プロジェクトのコピー
COPY hello-vue/ ./
RUN apk update
# Viteを実行
CMD ["npm", "run", "dev", "--", "--host"]