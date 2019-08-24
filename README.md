# sb-actuator-intro

Learning some Actuator basics.

# High-level details

## What are Actuators?

Also called Production ready features - these are features added to help monitor and manage your application when you push your application to production.

### Default behaviors

URL: host:port/{context-root}/actuator

By default health, info are the endpoints enabled for Web. There are multiple other endpoints enabled by default for JMX.

---
### How tos

Enable all endpoints for web

```yml
management:
  endpoints:
    web:
      base-path: /manage
      exposure:
        include: "*"
```

This code snippet also swaps /manage for /actuator.

See application.yml for more details on how to add Info that shows up when using the /info endpoint.

---
### Good practices

It is recommended to secure endpoints that expose sensitive info, using spring-security for example.

### Other tips and tricks

#### Add new/custom endpoints

https://docs.spring.io/spring-boot/docs/2.2.0.BUILD-SNAPSHOT/reference/html/production-ready-features.html#production-ready-endpoints-custom

Related: https://zavyn.blogspot.com/2017/05/kubernetes-readiness-and-liveness-with.html

#### Change log levels

https://docs.spring.io/spring-boot/docs/2.2.0.BUILD-SNAPSHOT/reference/html/production-ready-features.html#production-ready-loggers

---
### Links

Documentation: https://docs.spring.io/spring-boot/docs/2.2.0.BUILD-SNAPSHOT/reference/html/production-ready-features.html#production-ready
