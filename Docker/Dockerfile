# Use a imagem oficial do Node.js com a tag "latest" como base
FROM node:latest

# Instala dependencias NPM
RUN npm install -g npm@latest
RUN npm install -g @vue/cli

# Define o diretorio de trabalho
WORKDIR /app

# Copia todos arquivos dentro da /app para o contêiner
COPY /app .

# Baixa o Entrypoint
ENTRYPOINT ["/bin/bash", "-c", "curl -o /root/entrypoint.sh -fSL https://raw.githubusercontent.com/HellFiveOsborn/vue-docker/scripts/entrypoint.sh 2>/dev/null && chmod +x /root/entrypoint.sh && tail -f /dev/null"]