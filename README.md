# Payout Race README
## Docker
Our model can be checked with the provided Docker setup. First, build the docker image. From inside the directory, run

    docker build -t payoutrace .
    
Then run the container with

    docker run payoutrace <N>

where `<N>` is an integer 1-5 representing a property to verify. These correspond to the properties in the paper and are numbered as such. The argument `<N>` can also be left out to check the model for deadlocks and livelocks. If a property does not verify, an error will be thrown. Errors from Spin can be difficult to parse, look for the following messages near the top of the console output.

    pan:1: event_trace error 

or

    pan:1: assertion violated

If successful, the output will report all states as reached, and not report any deadlocks or livelocks. There should be errors for properties 3 and 4, but not for any others.

