# docker-laravel
Estructura base y configuraciones de docker para correr proyectos en Laravel

## Detalle con Node:
Para compilar el node y que funcione el Vite ejecuta lo siguiente:

docker exec -it ${PROJECT_NAME}_node sh

npm install
npm run build 
npm run dev
