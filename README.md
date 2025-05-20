# Taller de Microservicios V4

## Integrantes

- **Brayan Estiven Salcedo Suarez**
- **David Alejandro Calderon Pineda**

## Descripción General

Este proyecto forma parte del Taller de Microservicios V4. Se enfoca en la implementación de una arquitectura distribuida utilizando microservicios desarrollados en Django y desplegados en contenedores Docker, orquestados a través de un API Gateway (Kong). Además, se incorpora una Cloud Function programada con Cloud Scheduler para la ingesta automatizada de datos.

## Componentes del Proyecto

- **Microservicio Places**: Servicio REST para gestionar lugares. Permite registrar ubicaciones que serán validadas por el microservicio de mediciones.
- **Microservicio Measurements**: Encargado de registrar datos de oxígeno. Verifica si el lugar asociado existe a través del microservicio Places.
- **Kong API Gateway**: Encargado de enrutar solicitudes a los microservicios y proteger los endpoints.
- **Cloud Function**: Se encarga de generar automáticamente registros de datos de oxígeno cada cierto intervalo.
- **Cloud Scheduler**: Programa y activa periódicamente la ejecución de la Cloud Function.

## Diagrama de Despliegue

El proyecto incluye un **diagrama de despliegue actualizado**, el cual representa gráficamente la arquitectura final implementada.

Este diagrama incluye:

1. Todos los elementos indicados en la guía original.
2. El nuevo microservicio **Places**.
3. La **Cloud Function** conectada al **Cloud Scheduler**, y su integración con los microservicios existentes.
