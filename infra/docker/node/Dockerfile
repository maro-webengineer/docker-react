FROM node:22-alpine

WORKDIR /workspace

# ユーザーとグループIDを引数として受け取る
ARG UID=1000
ARG GID=1000

# nodeユーザーのUID/GIDを変更
RUN deluser --remove-home node \
  && addgroup -S node --gid ${GID} \
  && adduser -S -G node --uid ${UID} node

# nodeユーザーに切り替え
USER node

# 開発サーバーのポートを公開
EXPOSE 5173

# 開発サーバーを起動
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
