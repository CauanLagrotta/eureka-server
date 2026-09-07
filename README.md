# Eureka Server

Serviço de descoberta de serviços do projeto Saloon Platform.

## Visão Geral

O Eureka Server é responsável pelo registro e descoberta de todos os microsserviços da plataforma. Cada serviço se registra no Eureka e pode ser descoberto por outros serviços através do nome registrado.

## Porta

**8070**

## Funcionalidades

- Registro automático de serviços
- Descoberta de serviços por nome
- Monitoramento de saúde dos serviços
- Balanceamento de carga客户端

## Endpoints Importantes

- **Dashboard:** `http://localhost:8070`
- **Actuator Health:** `http://localhost:8070/actuator/health/readiness`
- **Eureka Apps:** `http://localhost:8070/eureka/apps`

## Tecnologias

- Spring Boot 4.1.0
- Spring Cloud Netflix Eureka Server
- Java 21

## Como Rodar

```bash
mvn clean package
java -jar target/eureka-server-0.0.1-SNAPSHOT.jar
```

## Configuração

O serviço se configura automaticamente via `application.yml`. Em produção, as configurações de porta e other podem ser ajustadas via variáveis de ambiente.

## Dependências

- Nenhuma dependência externa (é o primeiro serviço a subir)
