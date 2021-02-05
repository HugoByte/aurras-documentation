# Event Manager

The Event Manager is composed of multiple actions including using a database to store trigger URLs and their respective auth, and Kafka provider, consumer, and producer. Once the event manager receives an event from the event feed, this data is produced to a topic. The feed action in the manager lets the user hook into the system. That is, once an event is indexed to a particular topic, it can invoke a particular action. While creating the workflow, users can choose the event trigger as feed and provide necessary parameters from which chain it should be listening to.

