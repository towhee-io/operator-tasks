**Parameters:**

​**video:** *List[towhee.types.VideoFrame] (VideoFrame a sub-class of numpy.ndarray)*

Input video frames in ndarray.

**Returns:** *List[str], List[float], numpy.ndarray*

The return value is a tuple of (labels, scores, feature_vector). The lables are predicted class names. Scores are possibility scores ranking from high to low corresponding to predicted labels. Feature vector representing video features extracted by model 