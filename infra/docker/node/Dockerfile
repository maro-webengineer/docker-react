FROM node:22-alpine

# 作業ディレクトリ
WORKDIR /app

# ホットリロードでファイル監視を安定させるための環境変数
ENV CHOKIDAR_USEPOLLING=true \
    NODE_ENV=development

# Vite のデフォルトポート
EXPOSE 5173

# コンテナ起動時に dev サーバを立ち上げる
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0", "--port", "5173"]
