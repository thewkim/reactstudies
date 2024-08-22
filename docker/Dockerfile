# Usar a imagem Node.js Alpine como base
FROM node:18-alpine

# Definir o diretório de trabalho
WORKDIR /app

# Copiar o package.json e o package-lock.json
COPY package*.json ./

# Instalar as dependências
RUN npm install

# Copiar o restante do código do aplicativo
COPY . .

# Construir o aplicativo
RUN npm run build

# Expor a porta que o Vite usará
EXPOSE 5173

# Comando para iniciar o servidor de desenvolvimento
CMD ["npm", "run", "dev"]
