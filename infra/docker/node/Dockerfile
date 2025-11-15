FROM node:22-alpine

WORKDIR /workspace

# nodeユーザーに切り替え
USER node

# 開発サーバーのポートを公開
EXPOSE 5173

# 開発サーバーを起動
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
