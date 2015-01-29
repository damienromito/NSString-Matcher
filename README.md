# NSString-Matcher
An easy way to match NSString with a Regex 



    NSString *string = @"/sc/trovesband/youth_in_decay#https://api.soundcloud.com/tracks/162801570/stream";
    NSString *regex = @"(tracks)\\/([\\d]+)";

**Get the first or the only group**

    NSString *result = [string firstMatchedGroupWithRegex:regex];
    //result = tracks;

**Get a specific match**

    NSString *result = [string matchWithRegex:regex atIndex:2];
    //result = 162801570;

**Get all match**

    NSArray *results = [string matchWithRegex:regex];
    //results = ["tracks/162801570", "tracks", "162801570"] 

