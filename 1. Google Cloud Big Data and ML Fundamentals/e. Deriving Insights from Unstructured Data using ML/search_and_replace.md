Copy CSV file which contains the string `placeholder` in each row, reserved for your specific bucket name

`gsutil cp gs://spls/gsp223/data.csv .`

Find and replace placeholder with your bucket name globally

`sed -i -e "s/placeholder/${BUCKET}/g" ./data.csv`
