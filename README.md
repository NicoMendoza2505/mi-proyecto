# 🚀 Proyecto CI/CD - Ingeniería de Software II

PROFE ESTO LO SAQUE CON IA, LA GUIA YA ABRCA TODO Y DICE LO MISMO PERO LO QUE SI ME PUSO A LLORAR FUE LO DE LOS PERMISOS JAJAJA c:

## 📌 Descripción

Este proyecto implementa un pipeline de CI/CD utilizando GitHub y GitHub Actions para automatizar pruebas y despliegue de una aplicación Node.js con Express.

---

## 🛠 Tecnologías utilizadas

- Node.js
- Express
- Jest
- Supertest
- GitHub Actions
- GitHub Pages

---

## ⚙️ Integración Continua (CI)

Cada vez que se realiza un `push` a la rama `main`, el pipeline ejecuta automáticamente:

1. Instalación de dependencias (`npm ci`)
2. Ejecución de pruebas automatizadas (`npm test`)
3. Generación de reporte de cobertura

Si alguna prueba falla, el pipeline se detiene y el despliegue no se ejecuta.

---

## 🧪 Pruebas Automatizadas

Se implementaron pruebas para los siguientes endpoints:

- GET `/`
- GET `/health`
- GET `/version`
- GET `/creator`

Se utiliza Jest y Supertest para validar las respuestas del servidor.

---

## 🚀 Despliegue Continuo (CD)

Si todas las pruebas pasan correctamente, el pipeline:

1. Genera una página HTML de estado
2. La publica automáticamente en la rama `gh-pages`
3. GitHub Pages despliega el sitio

URL del sitio desplegado:

https://nicomendoza2505.github.io/mi-proyecto/


--

## ⚠️ Desafíos enfrentados

Uno de los principales problemas fue un error de permisos (403) al intentar hacer el deploy con GitHub Actions.

Se solucionó habilitando:
Settings → Actions → Read and write permissions.

También se presentaron problemas de indentación en el archivo YAML del workflow.

---

## 📂 Estructura del proyecto

mi-proyecto/
├── src/
├── tests/
├── .github/workflows/
├── package.json
└── README.md


---

## 🎯 Resultado

Se logró implementar un pipeline CI/CD funcional que automatiza:

Push → Tests → Deploy → Publicación automática

