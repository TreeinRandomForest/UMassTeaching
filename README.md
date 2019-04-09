# UMassTeaching
UMass Class on April 10, 2019

There are two notebooks. One contains all the exercises the students are supposed to carry out. The other contains solutions
and we can expose both to the students so they don't get stuck.

utils.py contains useful functions for the latter part of the notebook.


# Starting a Jupyter server

1. Access the JupyterHub URL
2. Select `s2i-scipy-notebook:3.6` from the dropdown list
3. Fill `foo` into `AWS_ACCESS_KEY_ID` and `bar` into `AWS_SECRET_ACCESS_KEY`
4. Click `Spawn`

# Cloning this repository

1. Click `New` on the right of the main view and select `Terminal`
2. Call following command:
    ```
    git clone https://github.com/TreeinRandomForest/UMassTeaching
    ```
3. Enter the newly created directory
    ```
    cd UMassTeaching
    ```
4. Create a `data` directory
    ```
    mkdir data
    ```

# Downloading Training Data

Data are stored in Ceph Object Storage which implements AWS S3 API. You have configure `aws` client tool by entering access key and secret key while spawning the server.

To download a training data set, run the following command:

```
aws --endpoint-url $S3_ENDPOINT_URL s3 cp s3://UMASS/train_sample.csv train_sample.csv
```

