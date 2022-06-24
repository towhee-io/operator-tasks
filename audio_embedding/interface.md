**Parameters:**

*data: List[towhee.types.audio_frame.AudioFrame]*

Input audio data is a list of towhee audio frames.


**Returns**:

*numpy.ndarray*

Audio embeddings in shape (num_clips, feature_dim).
Each embedding stands for features of an audio clip with fixed length.

