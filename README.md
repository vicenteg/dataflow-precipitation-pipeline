# Dataflow Precipitation Sample

## About

Both Google Dataflow and Google BigQuery can be tricky to use, let alone combining the two. This example pipeline uses both technologies extensively and implements several features (both simple and complicated) that you may need in your own project. Feel free to explore this example as you like. We hope it may serve some small part in furthering your endevours. 

### Data Source

All data comes from NOAA and can be found at http://water.weather.gov/precip/download.php
The BigQuery US Precipitation dataset is also continuously updated using this pipeline, and can be found at https://bigquery.cloud.google.com/table/publicdata:samples.us_precipitation

## Usage

### Credentials

If you do not already have Google cloud credentials setup, you'll need to install gcloud and run the command:

   $ gcloud auth login

This pipeline uses the default Google credentials.
You can find more about setting up Google credentials at https://developers.google.com/identity/protocols/application-default-credentials 

### Execution

To run this pipeline, simply run the command:

    $ java -jar PrecipPipe.jar --startDate=20150101 --endDate=20150709 --project=myProject --table=myProject:weather.precipitation --bucket=myBucket

For a full list of options, run:

    $ java -jar PrecipPipe.jar --help

Include the "--help=PrecipitationOptions" flag for a list of pipeline-specific options.

## License

This library is licensed under Apache 2.0. Full license text is
available in [LICENSE.txt](LICENSE.txt).

## Contributing

See [CONTRIBUTING](CONTRIBUTING.md).

## Support

Please [report bugs at the project on Github](https://github.com/google/google-api-ruby-client/issues). Don't
hesitate to [ask questions](http://stackoverflow.com/questions/tagged/google-api-ruby-client) about the client or APIs
on [StackOverflow](http://stackoverflow.com).
