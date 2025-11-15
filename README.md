# CST8915-lab7
## Lab 7 

### YouTube Demo Video
*(https://youtu.be/hshOkfJP7s0)*

## RabbitMQ Configuration Issues

Stateful or Stateless?
- Stateful

Problem with Current Configuration:
- No persistent storage (PVC)
- Uses Deployment instead of StatefulSet
- Data lost if pod restarts or is deleted

What Happens on Pod Deletion/Restart:
- All queues and messages are lost
- Order Service fails until queues are recreated

Potential Solutions:
- Add PersistentVolumeClaim
- Use StatefulSet
- Use RabbitMQ Helm chart
- Or replace with Azure Service Bus
