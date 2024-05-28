# BP-MAVEN-STEP

I'll use maven to build the java project


## Setup
* Clone the code available at [BP-MAVEN-STEP](https://github.com/OT-BUILDPIPER-MARKETPLACE/BP-MAVEN-STEP)
* Build the docker image

```
git submodule init
git submodule update
docker build -t ot/yarn:1.0 .
```

* Do local testing via image only
```
# install the dependencies  code with default settings 
docker run -it --rm -v $PWD:/src -e WORKSPACE=src -e CODEBASE_DIR=traya-form-v2 -e INSTRUCTION=install   ot/yarn:1.0

# to build the code
docker run -it --rm -v $PWD:/src -e WORKSPACE=src -e CODEBASE_DIR=. -e INSTRUCTION=build   ot/yarn:1.0

```