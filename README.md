# sagetesting
Test deployment of the open Cisco LLM model https://huggingface.co/fdtn-ai/Foundation-Sec-8B in a personal AWS account.  This work is not CISCO authored or approved, it is a trial to provide larger testing abilities to consumers of the new model.

1. Create a python venv based on the repo
2. create a sagemaker execution role in IAM
3. configure your boto3/AWS CLI environment with keys/secret keys to an IAM principal with enough priviledges to create
4. Run the python script
5. Wait about 5-10 minutes...you can look at the console or run ```aws sagemaker list-endpoints```.  You'll need the endpoint id to feed into the invoke commands in the next step.
6. play around/test with the invoke CLI command that runs AWS sagemaker invoke commands in CLI to feed in the testprompt and return the output.txt
7. Enjoy!
