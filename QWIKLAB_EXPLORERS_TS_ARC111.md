# Get Started with Cloud Storage: Challenge Lab || [ARC111](https://www.cloudskillsboost.google/focuses/62706?parent=catalog) ||

# # Like, comment, share & Don't forget to subscribe [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN) 👍😄🤝

### Run the following Commands in CloudShell

```
export BUCKET_1=
export BUCKET_2=
export BUCKET_3=
```

```
run_form_1() {

gsutil mb -c coldline gs://$BUCKET_1

gsutil retention set 30s gs://$BUCKET_2

echo "Awesome Lab" > sample.txt

gsutil cp sample.txt gs://$BUCKET_3
}

#form 2
# Function to run form 2 code
run_form_2() {

gsutil mb gs://$BUCKET_1

gcloud alpha storage buckets update gs://$BUCKET_2 --no-uniform-bucket-level-access

gsutil acl ch -u $USER_EMAIL:OWNER gs://$BUCKET$BUCKET_2

gsutil rm gs://$BUCKET$BUCKET_2/sample.txt

echo "Awesome Lab" > sample.txt

gsutil cp sample.txt gs://$BUCKET$BUCKET_2

gsutil acl ch -u allUsers:R gs://$BUCKET$BUCKET_2/sample.txt

gcloud storage buckets update gs://$BUCKET_3 --update-labels=key=value
}

#form 3
# Function to run form 3 code
run_form_3() {

gsutil mb -c nearline gs://$BUCKET_1

echo "This is an example of editing the file content for cloud storage object" | gsutil cp - gs://$BUCKET_2/sample.txt

gsutil defstorageclass set ARCHIVE gs://$BUCKET_3
}

# Main script block
echo "${WHITE}${BOLD}"

# Get the form number from user input
read -p "Enter Form Number (1, 2, or 3): " form_number

# Execute the appropriate function based on the selected form number
case $form_number in
    1) run_form_1 ;;
    2) run_form_2 ;;
    3) run_form_3 ;;
    *) echo "Invalid form number. Please enter 1, 2, or 3." ;;
esac

```

# Congratulations ..!!🎉  You completed the lab shortly..😃💯

# *Well done..!* 👏

# Thank you for visiting.... :) 🗯️

# [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN)
