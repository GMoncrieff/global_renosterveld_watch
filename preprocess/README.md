# `grw_preprocess`

## Building the Template
Make the build script executable with `chmod +x build.sh` and then run:
```bash
./build.sh
```

## Running the Template
Make the template run script executable with `chmod +x run_template.sh` and then run:
```bash
export GRW_PREPROCESS_INPUT="gs://reno-ee-example/NEW_Image_reno_predict__2021-07-0800008.tfrecord.gz"
export GRW_PREPROCESS_OUTPUT="gs://reno-ee-example/RealBeamOutput2"
./run_template.sh
```

Obviously you may need to change the environment variables `GRW_INPUT` and `GRW_OUTPUT` to match example data for yourself.

## Running Locally
First start by install grw_preprocess:
```bash
python setup.py develop
```

Next set your `GOOGLE_APPLICATION_CREDENTIALS` environment variable to point to your JSON credentials config,

Finally run:
```bash
export GRW_PREPROCESS_PROJECT="ee-vegetation-gee4geo"
export GRW_PREPROCESS_TEMP_LOCATION="gs://reno-ee-example/tmp/"
export GRW_PREPROCESS_STAGING_LOCATION="gs://reno-ee-example/staging/"
export GRW_PREPROCESS_INPUT="gs://reno-ee-example/NEW_Image_reno_predict__2021-07-0800008.tfrecord.gz"
export GRW_PREPROCESS_OUTPUT="gs://reno-ee-example/RealBeamOutput2"
./run_local.sh
```

Obviously you may need to change the environment variables to match your situation.