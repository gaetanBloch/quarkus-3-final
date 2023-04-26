# quarkus-3-final

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar target/*-runner.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./mvnw package -Pnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/quarkus-3-final-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.

## Related Guides

- OpenID Connect Client ([guide](https://quarkus.io/guides/security-openid-connect-client)): Get and refresh access tokens from OpenID Connect providers
- OpenID Connect Client Filter Reactive ([guide](https://quarkus.io/guides/security-openid-connect-client)): Use Reactive RestClient filter to get and refresh access tokens with OpenId Connect Client and send them as HTTP Authorization Bearer tokens
- Camel Quartz ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/quartz.html)): Schedule sending of messages using the Quartz 2.x scheduler
- SmallRye JWT ([guide](https://quarkus.io/guides/security-jwt)): Secure your applications with JSON Web Token
- Quarkus Extension for Spring Data JPA API ([guide](https://quarkus.io/guides/spring-data-jpa)): Use Spring Data JPA annotations to create your data access layer
- Elasticsearch REST client ([guide](https://quarkus.io/guides/elasticsearch)): Connect to an Elasticsearch cluster using the REST low level client
- Camel Microprofile Fault Tolerance ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/microprofile-fault-tolerance.html)): Circuit Breaker EIP using Microprofile Fault Tolerance
- JDBC Driver - PostgreSQL ([guide](https://quarkus.io/guides/datasource)): Connect to the PostgreSQL database via JDBC
- Keycloak Authorization ([guide](https://quarkus.io/guides/security-keycloak-authorization)): Policy enforcer using Keycloak-managed permissions to control access to protected resources
- Kubernetes Client ([guide](https://quarkus.io/guides/kubernetes-client)): Interact with Kubernetes and develop Kubernetes Operators
- Jacoco - Code Coverage ([guide](https://quarkus.io/guides/tests-with-coverage)): Jacoco test coverage support
- OpenTelemetry ([guide](https://quarkus.io/guides/opentelemetry)): Use OpenTelemetry to trace services
- Hibernate Search + Elasticsearch ([guide](https://quarkus.io/guides/hibernate-search-orm-elasticsearch)): Automatically index your Hibernate entities in Elasticsearch
- Hibernate Search Coordination with Outbox Polling ([guide](https://quarkus.io/guides/hibernate-search-orm-elasticsearch)): Use a transactional outbox and background polling to coordinate automatic indexing in Hibernate Search
- Reactive PostgreSQL client ([guide](https://quarkus.io/guides/reactive-sql-clients)): Connect to the PostgreSQL database using the reactive pattern
- Camel Syslog ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/syslog.html)): Marshall SyslogMessages to RFC3164 and RFC5424 messages and back
- Hibernate ORM ([guide](https://quarkus.io/guides/hibernate-orm)): Define your persistent model with Hibernate ORM and Jakarta Persistence
- Minikube ([guide](https://quarkus.io/guides/kubernetes)): Generate Minikube resources from annotations
- Apache Avro ([guide](https://quarkus.io/guides/kafka)): Provide support for the Avro data serialization system
- Camel iCal ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/ical.html)): Marshal and unmarshal iCal (.ics) documents to/from model objects
- Vault ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-vault/dev/index.html)): Store your credentials securely in HashiCorp Vault
- Kubernetes ([guide](https://quarkus.io/guides/kubernetes)): Generate Kubernetes resources from annotations
- SmallRye Context Propagation ([guide](https://quarkus.io/guides/context-propagation)): Propagate contexts between managed threads in reactive applications
- Camel OpenTelemetry ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/opentelemetry.html)): Distributed tracing using OpenTelemetry
- Eclipse Vert.x ([guide](https://quarkus.io/guides/vertx)): Write reactive applications with the Vert.x API
- Camel Kafka ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/kafka.html)): Sent and receive messages to/from an Apache Kafka broker
- SmallRye Reactive Messaging ([guide](https://quarkus.io/guides/reactive-messaging)): Produce and consume messages and implement event driven and data streaming applications
- Camel Bean Validator ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/bean-validator.html)): Validate the message body using the Java Bean Validation API
- Camel MicroProfile Health ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/microprofile-health.html)): Expose Camel health checks via MicroProfile Health
- Quartz ([guide](https://quarkus.io/guides/quartz)): Schedule clustered tasks with Quartz
- Narayana STM - Software Transactional Memory ([guide](https://quarkus.io/guides/software-transactional-memory)): Offer Software Transactional Memory (stm) support
- Liquibase ([guide](https://quarkus.io/guides/liquibase)): Handle your database schema migrations with Liquibase
- Redis Cache ([guide](https://quarkus.io/guides/cache-redis-reference)): Use Redis as the caching backend
- Kubernetes Config ([guide](https://quarkus.io/guides/kubernetes-config)): Read runtime configuration from Kubernetes ConfigMaps and Secrets
- Redis Client ([guide](https://quarkus.io/guides/redis)): Connect to Redis in either imperative or reactive style
- Camel Micrometer ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/micrometer.html)): Collect various metrics directly from Camel routes using the Micrometer library
- Cache ([guide](https://quarkus.io/guides/cache)): Enable application data caching in CDI beans
- Camel PDF ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/pdf.html)): Create, modify or extract content from PDF documents
- Narayana LRA - LRA Participant Support ([guide](https://quarkus.io/guides/lra)): Coordinate Long Running Actions (LRA)
- SmallRye Fault Tolerance ([guide](https://quarkus.io/guides/smallrye-fault-tolerance)): Build fault-tolerant network services
- Scheduler ([guide](https://quarkus.io/guides/scheduler)): Schedule jobs and tasks
- Camel Debezium PostgresSQL Connector ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/debezium-postgres.html)): Capture changes from a PostgresSQL database
- Apicurio Registry - Avro ([guide](https://quarkus.io/guides/kafka-schema-registry-avro)): Use Apicurio as Avro schema registry
- Camel JSON Path ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jsonpath.html)): Evaluate a JSONPath expression against a JSON message body
- Camel Jira ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jira.html)): Interact with JIRA issue tracker
- Camel PostgresSQL Event ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/pgevent.html)): Send and receive PostgreSQL events via LISTEN and NOTIFY commands
- SmallRye OpenAPI ([guide](https://quarkus.io/guides/openapi-swaggerui)): Document your REST APIs with OpenAPI - comes with Swagger UI
- DataStax Apache Cassandra client ([guide](https://quarkus.io/guides/cassandra)): Connect to Apache Cassandra, DataStax Enterprise and DataStax Astra databases
- SmallRye Reactive Messaging - Kafka Connector ([guide](https://quarkus.io/guides/kafka-reactive-getting-started)): Connect to Kafka with Reactive Messaging
- Hibernate ORM with Panache ([guide](https://quarkus.io/guides/hibernate-orm-panache)): Simplify your persistence code for Hibernate ORM via the active record or the repository pattern
- OpenID Connect Token Propagation ([guide](https://quarkus.io/guides/security-openid-connect-client)): Use Jakarta REST Client filter to propagate the incoming Bearer access token or token acquired from Authorization Code Flow as HTTP Authorization Bearer token
- Apache Kafka Streams ([guide](https://quarkus.io/guides/kafka-streams)): Implement stream processing applications based on Apache Kafka
- Reactive Routes ([guide](https://quarkus.io/guides/reactive-routes)): REST framework offering the route model to define non blocking endpoints
- Camel Mail ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/mail.html)): Send and receive emails using imap, pop3 and smtp protocols
- Mutiny ([guide](https://quarkus.io/guides/mutiny-primer)): Write reactive applications with the modern Reactive Programming library Mutiny
- Camel Cassandra CQL ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/cassandraql.html)): Integrate with Cassandra 2.0 using the CQL3 API (not the Thrift API). Based on Cassandra Java Driver provided by DataStax
- Camel File ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/file.html)): Read and write files
- REST Client Reactive ([guide](https://quarkus.io/guides/rest-client-reactive)): Call REST services reactively
- RESTEasy Reactive ([guide](https://quarkus.io/guides/resteasy-reactive)): A Jakarta REST implementation utilizing build time processing and Vert.x. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it.
- OpenID Connect Client Filter ([guide](https://quarkus.io/guides/security-openid-connect-client)): Use Jakarta REST Client filter to get and refresh access tokens with OpenId Connect Client and send them as HTTP Authorization Bearer tokens
- RESTEasy Reactive Links ([guide](https://quarkus.io/guides/resteasy-reactive#web-links-support)): Web Links support for RESTEasy Reactive. Inject web links into response HTTP headers by annotating your endpoint resources.
- Apache Kafka Client ([guide](https://quarkus.io/guides/kafka)): Connect to Apache Kafka with its native API
- YAML Configuration ([guide](https://quarkus.io/guides/config#yaml)): Use YAML to configure your Quarkus application
- Camel Caffeine Cache ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/caffeine.html)): Perform caching operations using Caffeine Cache
- OpenID Connect Token Propagation Reactive ([guide](https://quarkus.io/guides/security-openid-connect-client)): Use Reactive REST Client to propagate the incoming Bearer access token or token acquired from Authorization Code Flow as HTTP Authorization Bearer token
- Camel Bean ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/bean.html)): Invoke methods of Java beans
- Logging JSON ([guide](https://quarkus.io/guides/logging#json-logging)): Add JSON formatter for console logging
- SmallRye Health ([guide](https://quarkus.io/guides/smallrye-health)): Monitor service health
- Micrometer metrics ([guide](https://quarkus.io/guides/micrometer)): Instrument the runtime and your application with dimensional metrics using Micrometer.
- REST resources for Hibernate ORM with Panache ([guide](https://quarkus.io/guides/rest-data-panache)): Generate Jakarta REST resources for your Hibernate Panache entities and repositories
- Elasticsearch Java Client ([guide](https://quarkus.io/guides/elasticsearch)): Connect to an Elasticsearch cluster using the Java client
- Micrometer Registry Prometheus ([guide](https://quarkus.io/guides/micrometer)): Enable Prometheus support for Micrometer
- Hibernate Validator ([guide](https://quarkus.io/guides/validation)): Validate object properties (field, getter) and method parameters for your beans (REST, CDI, Jakarta Persistence)
- Logging GELF ([guide](https://quarkus.io/guides/centralized-log-management)): Log using the Graylog Extended Log Format and centralize your logs in ELK or EFK
- Camel Kubernetes ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/kubernetes.html)): Perform operations against Kubernetes API
- OpenID Connect ([guide](https://quarkus.io/guides/security-openid-connect)): Verify Bearer access tokens and authenticate users with Authorization Code Flow
- Security JPA ([guide](https://quarkus.io/guides/security-getting-started)): Secure your applications with username/password stored in a database via Jakarta Persistence

## Provided Code

### YAML Config

Configure your application with YAML

[Related guide section...](https://quarkus.io/guides/config-reference#configuration-examples)

The Quarkus application configuration is located in `src/main/resources/application.yml`.

### Hibernate ORM

Create your first JPA entity

[Related guide section...](https://quarkus.io/guides/hibernate-orm)

[Related Hibernate with Panache section...](https://quarkus.io/guides/hibernate-orm-panache)


### Reactive Messaging codestart

Use SmallRye Reactive Messaging

[Related Apache Kafka guide section...](https://quarkus.io/guides/kafka-reactive-getting-started)


### RESTEasy Reactive

Easily start your Reactive RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started-reactive#reactive-jax-rs-resources)

### SmallRye Health

Monitor your application's health using SmallRye Health

[Related guide section...](https://quarkus.io/guides/smallrye-health)
