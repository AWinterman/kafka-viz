# kafka-viz #

You're putting all this stuff in Kafka anyway, why not visualize it?

# Goal #

A lightweight consumer which samples from a subset of kafka topics. It also
runs a web service which visualizes the network of consumers and producers. Is
this possible?  Who knows? Let's find out!

# Structure #

This app has the following components.

- A consumer which implements a stream which emits update events. All of the
  logic concerning Kafka itself lives here.

- A lightweight server, preferably using websockets, which serves up a web page
  into which the data visualization will be drawn. 

- The data viz itself. For the time being this will be a lightweight d3
  force-directed graph. The graph will be rendered in svg, which probably
  limits us to around 100 nodes. If this is too few, we can add more later.
