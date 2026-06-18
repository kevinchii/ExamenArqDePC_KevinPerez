# Examen Final – Arquitectura de Computadores

## Objetivo
Diseñar, versionar, desplegar y eliminar una instancia EC2 en AWS de forma
automatizada usando CloudFormation y GitHub Actions, aplicando Git Flow.

## Tecnologías utilizadas
- AWS (EC2, CloudFormation, Security Groups)
- GitHub Actions
- Git / Git Flow

## Funcionalidad de Deploy
El workflow deploy.yml valida y despliega el template de CloudFormation,
creando una instancia EC2 con un Security Group con puerto 80 abierto
y una pagina web publicada automaticamente via UserData.

## Funcionalidad de Destroy
El workflow destroy.yml elimina el stack de CloudFormation, eliminando
la instancia EC2 y el Security Group creados.

## Template EC2
El archivo template/ec2.yaml define los recursos: una instancia EC2
Amazon Linux, un Security Group con puerto 80 habilitado, y un UserData
que instala Apache y publica una pagina web con los datos del estudiante.