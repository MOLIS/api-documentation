## Image sizes

For every uploaded image the API generates different (smaller) sizes. 

Example:

```
{
	original:"1bac96002cbe11e281c10800200c9a66.jpg",
	large:"1bac96002cbe11e281c10800200c9a66-large.jpg",
	medium:"1bac96002cbe11e281c10800200c9a66-medium.jpg",
	small:"1bac96002cbe11e281c10800200c9a66-small.jpg",
	thumb:"1bac96002cbe11e281c10800200c9a66-thumb.jpg"
}
```

#### original
The uploaded image. The API changed the filename, nothing else.

#### large
The uploaded image resized to fit in a box of 2048 x 1536 pixels.

#### medium
The uploaded image resized to fit in a box of 1024 x 768 pixels.

#### small
The uploaded image resized to fit in a box of 320 x 240 pixels.

#### thumb
The uploaded image cropped to fit in a box of 150 x 150 pixels.

### Notes

The API will **not** scale up the uplaoded images. However the API will still return all fields described as above. For example if you upload an image of size 1200x960px the object will look like this:

```
{
	original:"6f25ba702cc111e281c10800200c9a66.jpg",
	large:"6f25ba702cc111e281c10800200c9a66.jpg",
	medium:"1bac96002cbe11e281c10800200c9a66-medium.jpg",
	small:"1bac96002cbe11e281c10800200c9a66-small.jpg",
	thumb:"1bac96002cbe11e281c10800200c9a66-thumb.jpg"
}
```
`large` is the same as `original`.