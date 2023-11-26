#### CloudFront

    Two SSL = Viewer => Cloudfront , Cloudfront=>Origin

    Cloudfront and SNI.
    Every SSL enabled site needed its own IP.
    
    SNI allows multiple SSL sites to share the same IP.

    Viewer Protocol: client to distribution
    Can´t have self-signed certificate (public certificate only us-east-1)
    
    Origin Protocol: Cloudfront to origin
    Needs to use public trusted certificate. (s3 handle natively
    ALB needs the public certificate to talk with the cloudfront.

    Custom Origin can configure ports
    
    If you don´t forward & don't cache, the cache is created using the object name.
    More things involed in caching the less eficient it is.




