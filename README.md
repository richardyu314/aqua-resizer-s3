# aqua-resizer-s3
S3-compatible Aqua Resizer

Works the same way as https://github.com/syamilmj/Aqua-Resizer with the following additional steps:
(1) download the AWS PHP SDK from https://github.com/richardyu314/aqua-resizer-s3
(2) update line 17 ("require_once") to point to the absolute path of your AWS SDK installation's aws-autoloader.php (i.e., /var/www/html/aws/aws-autoloader.php")
(3) update $s3url on line 84 to point to the URL of your S3 or Cloudfront CDN (i.e., a888888.cloudfront.net). Do not use a trailing slash on this URL
(4) update lines 162 to 165 with your AWS credentials (S3 bucket name, IAM user key, IAM user secret) 

Note that for (3), this implementation assumes that your S3 bucket has a wp-content/uploads path set up. If your S3 bucket is configured differently, change lines 139 and 155 where  wp-content/uploads is referenced to your media directory in S3
