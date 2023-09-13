# Use a imagem oficial do Node.js com a tag "latest" como base
FROM node:latest

# Instala dependencias NPM
RUN npm install -g npm@latest
RUN npm install -g @vue/cli

# Copie o arquivo Docker/entrypoint.sh para o contêiner
COPY Docker/entrypoint.sh /root/entrypoint.sh

# Define o diretorio de trabalho
WORKDIR /app

# Copia todos arquivos dentro da /app para o contêiner
COPY /app .

# Mantenha o contêiner ativo
CMD ["tail", "-f", "/dev/null"]