# docker-admin-products
# 🚀 Admin Products App - Docker & Kubernetes Deployment

## 📌 Descripción

Este proyecto consiste en la contenerización y despliegue de una aplicación Full Stack de administración de productos utilizando Docker y Kubernetes.

La aplicación simula un entorno real donde se despliega un sistema compuesto por frontend, backend y base de datos, utilizando buenas prácticas de contenerización y orquestación.

---

## 🧠 Problema que resuelve

Permite desplegar una aplicación completa de gestión de productos en un entorno escalable y portable, simulando una arquitectura moderna utilizada en entornos productivos.

---

## 🏗️ Arquitectura

Frontend (React)
        ↓
Backend API (Node.js / Express)
        ↓
Base de datos (MySQL / MongoDB)

Despliegue:
Docker → Kubernetes (Pods, Services, Deployments)

---

## 🛠️ Tecnologías utilizadas

- Node.js
- React
- Docker
- Kubernetes
- YAML (manifiestos)
- Git & GitHub

---

## ⚙️ Funcionalidades

- CRUD de productos
- API REST para gestión de datos
- Interfaz web para administración
- Contenerización de servicios
- Orquestación con Kubernetes
- Comunicación entre servicios

---

## 🐳 Docker

La aplicación está completamente dockerizada, lo que permite:

- Ejecutar todos los servicios en contenedores
- Asegurar portabilidad entre entornos
- Facilitar despliegues consistentes

📌 Docker permite empaquetar aplicaciones con sus dependencias en contenedores ligeros y portables :contentReference[oaicite:0]{index=0}

---

## ☸️ Kubernetes

Se utilizan los siguientes recursos:

- Pods
- Deployments
- Services
- Configuración mediante archivos YAML

Kubernetes permite la orquestación de contenedores, facilitando la escalabilidad y gestión de aplicaciones distribuidas.

---


---

## 🚀 Cómo ejecutar el proyecto

### 1. Clonar repositorio

```bash
git clone https://github.com/JuanPabloQB1990/docker-kubernets-admin-products
```

```bash
cd docker-kubernets-admin-products
```
### 2. Ejecutar con Docker (debes tener docker instalado en tu maquina)

```bash
docker-compose up --build
```

### visualizar pagina ejecuta la siguiente URL:

```bash
http://localhost:5173/
```

### 3. Ejecutar con Kubernetes en orden (debes tener kubernetes instalado en tu maquina y luego ejecuta estos comandos para crear los deployment de cada servicio)

```bash
kubectl apply -f secret.yaml
```
```bash
kubectl apply -f persistence-db.yaml
```
```bash
kubectl apply -f configmap.yaml
```
```bash
kubectl apply -f deploy-db.yaml
```

```bash
kubectl apply -f persistence-db.yaml
```
```bash
kubectl apply -f deploy-backend.yaml
```
```bash
kubectl apply -f deploy-frontend.yaml
```

### 4. Para visualizar la pagina funcionando debes ingresar la siguiente URL: http://ip_cluster_kubernetes:puerto_servicio_frontend

```bash
http://192.168.49.2:30007/
```




