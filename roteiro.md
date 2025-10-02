Criar .env
MONGO_URI="mongodb+srv://......"
JWT_SECRET="senha_super_forte"

npm init -y
npm install express mongoose dotenv bcryptjs jsonwebtoken nodemon --save

W8espGEL3Wvxdgcu

Testar no Postman

1) Acessar localhost:3000/alunos

2) Registrar usuário

POST → http://localhost:3000/auth/register
Body JSON: { "username": "andre", "password": "123", "role": "admin" }

3) Fazer login
POST → http://localhost:3000/auth/login
Body JSON: { "username": "andre", "password": "123" }
Vai retornar um token JWT.

4) Acessar rota protegida
GET → http://localhost:3000/alunos
Headers → Authorization: Bearer <token>