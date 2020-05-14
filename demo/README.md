# Running Shiny app on Google Cloud Run

```
PROJECTID=$(gcloud config get-value project)
```

Build the app
```
gcloud builds submit --tag gcr.io/$PROJECTID/shinydemo
```

Deploy the app
```
gcloud run deploy --image gcr.io/$PROJECTID/shinydemo --platform managed --max-instances 1 --memory 1G
```
