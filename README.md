# aw08

Please extend your WebPOS system by adding a delivery service shown as the following figure (it's not necessary that your WebPOS system has a same layout of microservices as in this figure).

![](10-pos.svg)

When an order is placed by a user, the order serivce sends out an event into some AMQP MOM (such as RabbitMQ). The delivery service will be notified and a new delivery entry will be generated automatically. User can query the delivery status for his orders.

Use [Spring Cloud Stream](https://spring.io/projects/spring-cloud-stream) to make the scenerio happen. You can refer to the [guide project](https://github.com/spring-guides/gs-spring-cloud-stream) for technical details.