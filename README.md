# family_photos_json_server

## About this project

This is a place we put photos for the parent's anniversary. Below are instructions how to use the system.

## How to make an event page

That is done by making a special file of type `.json` inside `/events` folder. All files should be in that folder, the files should not be inside any other folders.

The `.json` file has the following structure:

```{json}
{
	"content" : [
	// All components go into here
	]
}
```
The components available are listed below.
Notice that all components must be ordered. The first component will be the first to be drawn on the website.
Take a note of the name of the `.json` file. It should be unique in the folder. The name should be in one word. If you have to make it of a few words use `camelCase`.

#### List of components

##### Empty Space
If you want to add a bit of an empty space to the event page that is the way to do it.
Add this code to the JSON in the `event.json`file.
```{json}
["emptySpace" : []],
```
 There are no parameters, but the empty array ***must*** be set.
 
 
 ##### Separation Line
You can add a separation line between different components of the event page.
Add this code to the JSON in the `event.json`file.
```{json}
["line" : []],
```
 There are no parameters, but the empty array ***must*** be set.
 
 
  ##### Event Title
Though you can add this compoent many times, I encourage you to add it only as the first element on every event page. That is a component that displays the name of the event.
Add this code to the JSON in the `event.json`file.
```{json}
["eventTitle" : ["Event Name"]],
```
 There is one required parameter. That parameter is the name of the event.
 
 
   ##### Quote
That is a piece of text that will be at the center of the page. The text will be in quatation marks.
Add this code to the JSON in the `event.json`file.
```{json}
["quote" : ["quote text"]],
```
 There is one required parameter. That parameter is the text of the quote.
 
 
 ##### Image-Quote
That is a component that combines a picture and a quote. Quote is optional here. Also, you can optionally set text underneath the picture. That text will go into two lines.
Add this code to the JSON in the `event.json`file.
```{json}
["imageQuote" : ["imageUrl", "topText", "bottomText" , "quoteText", imageRight? ]],
```
All parameters must be set for the code to work. If you do not want to have some text displayed onto the screen, you can simply leave it as `""` (empty string).
Here is a list of the parameters in the correct order:
1. `imageUrl` - Url of the image that will be displayed onto the screen. It must be set.
2. `topText` - That is the text underneath the image. This text will take the topmost line under the image. If you do not want *any* text underneath the image set this parameter to `""`. Then the code will not check what is stored in the `bottomText`.
3. `bottomText` - That is the text underneath the image on the bottommost line. If you do not want this text just set it to `""`
4. `quoteText` -  text of the quote. If you do not want this text just set it to `""`
5. `imageRight` - that is a boolean flag that tells whether you want image be on the right of the screen or on the left. Set this either to `true` or `false`.


##### Floating Images
That is a slide show of images that go from the left to the right of the screen, It is increadibly heavy for the system to process, so please do not use more than 7 images for it.
Add this code to the JSON in the `event.json`file.
```{json}
["floatingImages" : ["ImageUrls", "imageUrl", ...]],
```
 Inside the `[]` you must list all image URLs of images that you want in your slideshow.
 
 
 ##### Image Gallery
That is a grid of images. It is a perfect way to display a large number of images. There is no particular limit to the number of images.

Add this code to the JSON in the `event.json`file.
```{json}
["imageGallery" : ["ImageUrls", "imageUrl", ...]],
```
 Inside the `[]` you must list all image URLs of images that you want in your gallery.
 
 
###  Sample Event code
```{json}
{
    "content":[
        ["eventTitle", ["Свадьба"]],
        ["emptySpace", []],
        ["quote", ["Пусть все будет хорошо"]],
        ["emptySpace", []],
        ["floatingImages", [ "https://adtimokhin.github.io/family_photos_json_server/images/pexels-phil-desforges-15185102.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-feyza-yıldırım-16407235.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-polina-kovaleva-5546810.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-satumbo-16462830.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-jhonny-salas-brochero-16041156.jpg"]],
        ["line", []],
         ["imageQuote", ["https://adtimokhin.github.io/family_photos_json_server/images/pexels-ds-stories-6005016.jpg", "Top Text", "Text on the bottom", "Quote", true]],
         ["line", []],
        ["imageGallery", [
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-phil-desforges-15185102.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-feyza-yıldırım-16407235.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-polina-kovaleva-5546810.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-satumbo-16462830.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-jhonny-salas-brochero-16041156.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-elif-kaya-13536123.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-polina-tankilevitch-6988658.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-ds-stories-6005016.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-jaime-reimer-15953915.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-sevil-yeva-15895540.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-phil-desforges-15185102.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-feyza-yıldırım-16407235.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-polina-kovaleva-5546810.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-satumbo-16462830.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-jhonny-salas-brochero-16041156.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-elif-kaya-13536123.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-polina-tankilevitch-6988658.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-ds-stories-6005016.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-jaime-reimer-15953915.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-sevil-yeva-15895540.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-phil-desforges-15185102.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-feyza-yıldırım-16407235.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-polina-kovaleva-5546810.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-satumbo-16462830.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-jhonny-salas-brochero-16041156.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-elif-kaya-13536123.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-polina-tankilevitch-6988658.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-ds-stories-6005016.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-jaime-reimer-15953915.jpg",
            "https://adtimokhin.github.io/family_photos_json_server/images/pexels-sevil-yeva-15895540.jpg"
          ]],
         ["line", []],
         ["emptySpace", []]
        
    ]
}
```

Here is a [link](https://adtimokhin.github.io/anniversary/event/wedding/l_0) to see how that looks like on the web.

Notice how image Urls are specified.

### After you made the `.json` file

After you made `.json` file in the `/events` folder you must add the link to that file inside `events_summary.json` under the root folder.

Start by making a new event in the file `events_summary.json`:

```{json}
{
  "startYear": 2003,
  "startMonth": 5,
  "endYear": 2023,
  "endMonth": 5,
  "events": [
	// ... other events that happened before June of 2013 ...
    {
      "topText": "Event name",
      "bottomText": "YYYY MMM",
      "eventLink": "name_of_the_json_file",
      "year": 2013,
      "month": 6
    },
	// ... other events that happened after June of 2013 ....
  ]
}
```

#### Let's go over what these parameters are in the event object.
1. `topText` - That is the text that will appear in a card on the timeline. It will be on the top of the card. This text should indicate what this event is. It can be one or more words. Try to make it at most two words.
2. `bottomText` - That is the text that will appear in the card but at the bottom. Use it to display what time period that is (mark the start of that period). It should be given in a format year month `YYYY MMM` (Month will be a three letter representation).
3. `eventLink` - that is the name of the `.json` file that contains the structure of the event page.
4. `year` - number that indicates during what year this event has happened.
5. `month` - number that indicates the event's month. (should be in range from 1(Jan) to 12(Dec) ).

#### Updating other parts of the `events_summary.json` file
- Make sure that the event you added is placed in the correct place. The events should be in a chronological order, with earlier events being closer to the start of the list.
- If the event you added happened earlier or later than previoulsy stored events you must update   `startYear`, `startMonth`, `endYear`, `endMonth`at the *top* of the file. These four variables must match the range of the values in the events.

### Setting colors to the tile
That can be done in the same events that your were just updating to set the name of the event. That is how the customized tile will look like:

```{json}
{
  "startYear": 2003,
  "startMonth": 5,
  "endYear": 2023,
  "endMonth": 5,
  "events": [
	// ... other events that happened before June of 2013 ...
    {
      "topText": "Event name",
      "bottomText": "YYYY MMM",
      "eventLink": "name_of_the_json_file",
      "year": 2013,
      "month": 6,
	  "settings":{
        "textColor": "#F3E400",
        "hoverTextColor": "#FFEF02",
        "bgColor": "#e4e4e4",
        "hoverBgColor": "##f2f2f2",
		"size":200
      }
    },
	// ... other events that happened after June of 2013 ....
  ]
}
```
Notice that you can skip any part of the settings you do not want to change. You can even skip `settings` as a whole. There are predefined values for every attribute. They are:

- `textColor` - `#9DA3A3`
- `hoverTextColor` - `#CFD6D6`
- `bgColor` - `transparent`  <-- Special word which make the background transparent.
- `hoverBgColor` - `#1A1A1A`
- `size` - 200

Here is a quick overlook at the settings:
- `textColor` - Color of the text before user hovers over the tile. Should be given as a hexadecimal value.
- `hoverTextColor` - color of the text when user hovers over the tile. Should be given as a hexadecimal value.
- `bgColor` - Color of the background before user hovers over the tile. Should be given as a hexadecimal value
- `hoverBgColor` -  Color of the background before when hovers over the tile. Should be given as a hexadecimal value
- `size` - size of the tile in px. It set to 200px and it probably should stay like that. Otherwise it does not look too good. Should be a whole number, positive

### Adding new images

All images that you will be using in the event pages should be stored in `/images` folder. All files should have unique names, There are no any other constraints.


### Deploying the changes
The changes will be automatically deployed to the server, but it will take ~5 mins. You can see if your file was updated by entering the file's URL:

To see any changes to the `events_summary.json` follow this URL:
```
https://adtimokhin.github.io/family_photos_json_server/events_summary.json
```

If you want to see the event page `name.json` you can follow this URL:

```
https://adtimokhin.github.io/family_photos_json_server/events/<NAME_OF_FILE>.json
```
