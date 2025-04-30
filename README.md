# sagetesting
Test deployment of the open Cisco LLM model https://huggingface.co/fdtn-ai/Foundation-Sec-8B in a personal AWS account.  This work is not CISCO authored or approved, it is a trial to provide larger testing abilities to consumers of the new model.

All of this works great in cloudshell if you don't have a prepared environment with awscli, boto3, and sagemaker installed
1. Create a python venv based on the repo (optional)
2. create a sagemaker execution role in IAM.  I suggest the role name "sagemaker_execution_role"
3. configure your boto3/AWS CLI environment with keys/secret keys to an IAM principal with enough privledges to create  (```aws configure```)
4. Run the python script.  This will generate the model, the endpoint, and the endpoint policy entities in AWS.
5. Wait about 5-10 minutes...you can look at the console or run ```aws sagemaker list-endpoints```.  You'll need the endpoint id to feed into the invoke commands in the next step.
6. play around/test with the invoke CLI command sample that runs AWS sagemaker "invoke-model" commands using the CLI to feed in the testprompt and return the output.txt.  The testprompt data MUST BE in json format.  The output will also be in json format.
7. Enjoy!  I hope to whip up a simple query prompt tool that pretty prints the response.

   No AI was used for this;)  I borrowed and modified some one else's code like the olden days.
