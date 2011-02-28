# AWS SES Rake Tasks

Tasks to manage your Amazon Simple Email Service account. These tasks depend on the [aws-ses gem](http://github.com/drewblas/aws-ses).

## Access Keys

Before you can use these tasks you must setup your access keys. This can be done by doing one of the following:

Set the `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` environment variables to the corresponding keys

Set the `AWS_CREDENTIALS_FILE` environment variable to a file containing your keys in the following format:  

    AWSAccessKeyId=YourKeyId
    AWSSecretKey=YourSecretKey

## Address Management

    rake ses:addresses:delete  # Delete the verified address in EMAIL
    rake ses:addresses:list    # List verified addresses
    rake ses:addresses:verify  # Submit a verification request for the address in EMAIL

## Send Statistics & Quota 

    rake ses:info:quota        # Display send rates
    rake ses:info:statistics   # Display send statistics for the past 2 weeks
