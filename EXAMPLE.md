
```
gcloud builds submit event-handler --config=event-handler/cloudbuild.yaml --project $PROJECT_ID
gcloud run deploy event-handler --image gcr.io/fourkeys-386218/event-handler:lates

gcloud builds submit bq-workers --config=bq-workers/parsers.cloudbuild.yaml --project $PROJECT_ID --substitutions=_SERVICE=github
gcloud builds submit bq-workers --config=bq-workers/parsers.cloudbuild.yaml --project $PROJECT_ID --substitutions=_SERVICE=circleci
```