<h1 align="center">ROMs Hub</h1>

Simple app to keep all the custom ROMs and kernels for devices at one place. In order to add a project you should follow a next structure

Repository root dir
```
|
├── **/Brand** (This should contain a brand name e.g Samsung, Xiaomi, OnePlus...
|	├── **Device code name**
|	|	|
|	|	├── **Project type** (Kernel, ROM, or anything else)
|	|	|	|
|	|	|	├── **Project name** (e.g LineageOS 16. Fraco kernel r.41...)
|	|	|	|	|
|	|	|	|	├── **logo.png** (Logo must be 192x192 in PNG format)
|	|	|	|	|
|	|	|	|	└── **project.json** (This is a file which holds the project attributes)
|	|	|	|
|	|	|	├── (Another project name)
|	|	|	|
|	|	|	├── (Another project name)
|	|	|
|	|	|
|	|	├── **device_icon.png** (This is a device icon shown on a device list for a particular brand, my recommendation is to take a picture for GSMArena and resize it to 192x(anything smaller or equal to 192) in PNG format)
|	|    	|
|	|	├── (Another project type)
|	|
|	|
|	|
|	|
|	└──	**brand_icon.png** (This is an image shown in main list of device brands, it should be 192x192 in PNG format)
|
├── (Another brand)
|
├── (Another brand)
.
.
.
```

## Configure main.json
Then it's time to populate JSON file in order to get all content of your project, this JSON file get all of those, 
this is some basic example of how the structure of JSON file should look, looks similar to a directory structure you done above.
``` 
"brand":{
      "Xiaomi":[
         {
            "brand_icon":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/brand_icon.png",
            "begonia":{
               "device_model":"Redmi Note 8 pro",
               "device_icon":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/begonia/device_icon.png",
               "Kernels":{
                  "project_type_icon":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/resources/icons/placeholder.png",
                  "project_json":[
                     "https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/begonia/kernels/project1/project.json",
                     "https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/begonia/kernels/project2/project.json"
                  ]
               },
               "Roms":{
                  "project_type_icon":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/resources/icons/placeholder.png",
                  "project_json":[
                     "https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/begonia/roms/project1/project.json",
                     "https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/begonia/roms/project2/project.json"
                  ]
               }
            },
            "lavander":{
               "device_model":"Redmi Note 8 pro",
               "device_icon":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/lavander/device_icon.png",
               "Kernels":{
                  "project_type_icon":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/resources/icons/placeholder.png",
                  "project_json":[
                     "https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/lavander/kernels/project1/project.json",
                     "https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/lavander/kernels/project2/project.json"
                  ]
               },
               "Roms":{
                  "project_type_icon":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/resources/icons/placeholder.png",
                  "project_json":[
                     "https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/lavander/roms/project1/project.json",
                     "https://raw.githubusercontent.com/Paget96/ROMsHub/master/Xiaomi/lavander/roms/project2/project.json"
                  ]
               }
            }
         }
      ],
      "Samsung":[
         {
            "brand_icon":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/Samsung/brand_icon.png"
         }
      ]
   }
```

## Configure project.json
This file contains all the informations about the project you added, and it's structure is simple:
```
{
   "data":[{
      "id":"identification_placeholder",
      "name":"Project name",
	  "update_date":"10.Jan.2020",
      "banner":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/resources/icons/placeholder.png",
	  "logo":"https://raw.githubusercontent.com/Paget96/ROMsHub/master/resources/icons/placeholder.png",
      "short_description":"Some short description related to the project",
      "description":"Some description related to the project",
      "developer_name":"DevName",
      "source_git":"https://github.com",
      "forum_thread":"https://forum.xda-developers.com",
      "telegram":"https://t.me/Paget96"
   }]
}
```

When you are done, create a pull request and I'll do a check soon as possible and get your project live in application.
