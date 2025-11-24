# Petapa OnTrack

## Descripción
Petapa OnTrack es una plataforma web diseñada para brindar información sobre los tiempos de espera y los detalles de las atracciones del IRTRA Petapa. Su objetivo es resolver la problemática de desinformación que enfrentan los visitantes al no contar con datos sobre las atracciones, incluyendo el tiempo de espera de las mismas. La solución integra un frontend interactivo, un backend que gestiona y sirve la información del sistema, y un conjunto de modelos de predicción entrenados con datos históricos que estiman los tiempos de espera.

## Tecnologías Utilizadas
- **Frontend**: Next.js 15 (App Router), React 19, Tailwind CSS 4, DaisyUI, Motion , react-zoom-pan-pinch, react-icons.
- **Backend/BaaS**: PocketBase.
- **Data Science**: Python 3.10+, pandas, numpy, scikit-learn, joblib, requests, python-dotenv, Jupyter Notebooks para EDA y entrenamiento.
- **Infraestructura y herramientas**: Conda / virtualenv, Node.js 18+, npm 9+, World Weather Online API para features climáticas.

## Requisitos Previos
- Node.js 18+
- npm 9+
- Python 3.10+
- Conda

## Instalación

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/Kojimena/PG-2025-`21199`.git
   cd PG-2025-`21199`
    ```
2. Instalar dependencias del frontend:
    ```bash
    cd src/frontend
    npm install
    ```
3. Instalar dependencias del módulo de data science:
    ```bash
    cd ../ds
    conda env create -f environment.yml   # o python -m venv .venv && pip install -r requirements.txt
    ``` 
4. Configurar variables de entorno:
   - Frontend: Crear `.env.local` en `src/frontend/` con `NEXT_PUBLIC_PB_URL`.
   - Data Science: Crear `.env` en `src/ds/` con `CLIMATE_API_KEY`, `PB_URL`, `PB_ADMIN_EMAIL`, `PB_ADMIN_PASSWORD`.
5. Configurar PocketBase:
   - Levantar servidor local o usar instancia en la nube.
   - Crear colecciones `games`, `walkthrough`, `faqs` según el modelo de datos esperado.
6. Correr el frontend:
   ```bash
   cd ../frontend
   npm run dev
   ```
   Abrir `http://localhost:3000` en el navegador.

## Demo
El video demostrativo se encuentra en: [Demo Petapa OnTrack](/demo/demo.mp4)

## Documentación
El informe final del proyecto está disponible en: [Informe Final Petapa OnTrack](/docs/informe_final.pdf)

## Autores
- Jimena Hernández (GitHub: Kojimena)

## Licencia
License: MIT

