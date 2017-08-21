# NodeJS Cluster Example

## Description
The point of the current repository is to:
- Show an example of the NodeJS Cluster module
- Measure the difference in performance between using and not using multiple processes

## What are Clusters?

# Install the project
1. Clone the repository:
  - SSH: `git clone git@github.com:smoroso/nodejs-cluster-example.git`
  - HTTPS: `git clone https://github.com/smoroso/nodejs-cluster-example.git`
2. Navigate to the cloned repository: `cd nodejs-cluster-example`
3. Run `npm install` to install the dependencies

# Run the project
## Using multiple processes
`npm run multi-processes`

## Using a single process
`npm run single-process`

# Test the performance
1. In one tab, start the project with a single process or multiple processes
2. In another tab, run the test code: `ab -n 10000 -c 100 -k http://localhost:3000/`
3. Stop the project and start it again but this time with the other type to test
4. Run again the benchmark code in the other tab: `ab -n 10000 -c 100 -k http://localhost:3000/`
5. Compare the different metrics in both cases

Important metrics are:
- Time taken for tests
- Requests per second
- Time per request
- Transfer Rate
- Longest request

Note:
[ApacheBench (ab)](https://www.npmjs.com/package/ab) is already installed on macOS. If you are not on macOS, just run `npm install ab`
Documentation is available [here](https://httpd.apache.org/docs/2.4/programs/ab.html)

# Useful sources:
- [NodeJS Documentation for the cluster module](https://nodejs.org/api/cluster.html)
- [Scaling - Clustering in NodeJS](http://dealwithjs.io/scaling-clustering-in-node-js/)
