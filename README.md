
# Nginx Inception

3 layers of Nginx

### Layers

Just 1 nginx instance to load-balance on layer 2.

Layer 2 uses 3 nginx instances which load-balance again to layer 3.

Layer 3 usess a total of 9 nginx instances (3 for each instance in layer 2).
Each layer 3 instance sends its own result.

In total this inception consists of 13 nginx instances, all of them creating logs.

### Elastic

The main use of this project is to create absurd amounts of log traffic to load-test an elastic cluster.
