# Mongo Replica Set with Keyfile Auth

This repo contains the resources required to deploy a Mongo replica set in Railway from a template.

To deploy your own Mongo replica set in Railway, just click the button below!

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/gFmvuY)

For even more information, check out the tutorial in Railway:  [Deploy and Monitor a MongoDB Replica Set](https://docs.railway.app/tutorials/deploy-and-monitor-mongo)

### About the MongoDB Nodes
The MongoDB nodes in the replica set are built from the [Mongo CE image in Docker Hub](https://hub.docker.com/_/mongo).  The only customization to the image, is the inclusion of a [Keyfile](https://www.mongodb.com/docs/manual/tutorial/deploy-replica-set-with-keyfile-access-control/) to enable authentication.

### About the Init Service
The init service is used to execute the required command against MongoDB to initiate the replica set.  Upon completion, it deletes itself via the Railway public API.

## Example Apps

Included in this repo are some example apps to demonstrate how to connect to the replica set from a client.
- [Node app](/exampleApps/node/)
- [Python app](/exampleApps/python/)

## Contributions

Pull requests are welcome.  If you have any suggestions for how to improve this implementation of MongoDB replica sets, please feel free to make the changes in a PR.