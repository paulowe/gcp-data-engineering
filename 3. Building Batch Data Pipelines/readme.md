## Lift and Shift Hadoop, Spark to Dataproc Lab

git -C ~ clone https://github.com/GoogleCloudPlatform/training-data-analyst

~/training-data-analyst/quests/sparktobq/\*.ipynb

To locate the default Cloud Storage bucket used by Cloud Dataproc enter the following command in Cloud Shell:

export DP_STORAGE="gs://$(gcloud dataproc clusters describe <CLUSTER-NAME> --region=us-central1 --format=json | jq -r '.config.configBucket')"

Find and Replace Globally

`sed -i -e "s/YOUR_PROJECT_ID/$(gcloud config get-value project)/g" query.py`
