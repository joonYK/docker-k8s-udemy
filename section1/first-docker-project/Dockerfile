# node.js를 기본 이미지로 사용
FROM node:14

# 컨테이너의 파일 시스템 지정. (모든 컨테이너에는 자체 파일 시스템이 존재)
# 파일 시스템에 디렉토리를 지정.
WORKDIR /app

# WORKDIR 디렉토리에 package.josn을 복사
COPY package.json .

# npm install 명령 실행. 
RUN npm install

# 지정한 위치의 파일들을 다 복사. (app.mjs, helpers.mjs)
COPY . .

# 3000 포트로 연다. (app.mjs에서 3000포트로 수신하기 때문에)
EXPOSE 3000

# node 명령으로 app.mjs를 실행.
CMD ["node", "app.mjs"]