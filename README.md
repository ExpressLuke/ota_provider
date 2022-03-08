Simple automated LineageOS OTA provider 

**Requirements**: 
- jq
- gh
- unzip
- git


Up upload rom and generate jsom simply run 
```source release.sh ../path/to/lineageos.zip```

if you want to host this on your own git you can change ```URL=``` value inside of ```release.sh```

On device side changes either add overlay for `updater_server_url`or add prop ```lineage.updater.uri```  that points to json 
e.g. ```lineage.updater.uri=https://raw.githubusercontent.com/8890q/ota_provider/master/19.0/{device}.json```

do note you can either hardcode {device} or leave it to updater to handle that tho in that case user might break otas by changing props


todo: hanlde version bumps from 19.0 to 19.1 without manual edits
