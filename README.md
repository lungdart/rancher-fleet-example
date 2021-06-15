# rancher-fleet-example
This repo is an example of using fleet within rancher to automate continuous deployment.

## Usage
1. Create a new EKS cluster in your rancher space (Or use an existing one you have credentials installed for)
2. Create the following namespaces on each cluster you'd like to deploy to (Ideally within their own projects)
  * production
  * staging
  * dev
3. Deploy this repository using fleet (Rancher continuous deployment pipeline)
  * Remember that master branch is now main branch
  * Leave the path as the root
  * Select whatever clusters or cluster groups you'd like to deploy to.
4. Grab the new load balancer external hostnames from the links in the service menu
5. Update the CNAME records to point to the external hostnames AWS has given
6. Enjoy!

## Credits
Credit to https://github.com/paulbouwer/hello-kubernetes for supplying a great example container to deploy with!
