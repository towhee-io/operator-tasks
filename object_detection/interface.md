**Parameters:**

**data:** *towhee.types.Image (a sub-class of numpy.ndarray)*

Image data in ndarray format.

**Returns:** *List[(int, int, int, int)], List[str], List[float]*

The return value is a tuple of (boxes, classes, scores). The boxes is a list of bounding boxes. Each bounding box is represented by the top-left and the bottom right points, i.e. (x1, y1, x2, y2). The classes is a list of prediction labels. The scores is a list of the confidence scores.