**Parameters:**

**img:** *towhee.types.Image (a sub-class of numpy.ndarray)* 

The image need to be cropped.

**bboxes:** *numpy.ndarray* 

The bounding boxes for cropping. It's an ndarray with shape (n, 4), each row is formatted as (x1, y1, x2, y2).

**Returns**: *towhee.types.Image (a sub-class of numpy.ndarray)* 

The cropped image data as numpy.ndarray.
