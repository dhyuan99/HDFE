<h1 align='center' style="text-align:center; font-weight:bold; font-size:2.0em;letter-spacing:2.0px;"> Decodable and Sample Invariant Continuous Object Encoder </h1>

<p align='center' style="text-align:center;font-size:1.25em;">
    <a href="https://www.cs.umd.edu/~dhyuan" target="_blank" style="text-decoration: none;">Dehao Yuan</a>&nbsp;,&nbsp;
    <a href="https://http://furong-huang.com" target="_blank" style="text-decoration: none;">Furong Huang</a>&nbsp;,&nbsp;
    <a href="http://users.umiacs.umd.edu/~fer/" target="_blank" style="text-decoration: none;">Cornelia Fermüller</a>&nbsp;,&nbsp;
    <a href="http://users.umiacs.umd.edu/~yiannis/" target="_blank" style="text-decoration: none;">Yiannis Aloimonos</a>&nbsp;&nbsp;
</p>

<p align='center';>
<b>
<em>arXiv-Preprint, 2023</em> &nbsp&nbsp&nbsp&nbsp <a href="" target="_blank" style="text-decoration: none;">[arXiv]</a>
</b>
</p>

### Abstract
We propose Hyper-Dimensional Function Encoding (HDFE). **Left**: Given samples of a continuous object (e.g. a function), HDFE encodes the object into a fixed-length vector without any training. The encoding is not affected by the distribution and size with which the object is sampled. The encoding can be decoded to reconstruct the continuous object. **Right**: Applications of HDFE. HDFE can be used to perform machine learning tasks (e.g. classification, regression) on continuous objects. HDFE also enables neural networks to regress continuous objects by predicting their encodings.

<img src="assets/teasor.drawio.jpg" alt="abstract" style="width:auto;">

### Gain some Insights of HDFE
**Reconstruction of Function Encoding:**  Under a suitable selection of receptive field and dimensionality, HDFE can produce a decodable encoding of the original function. **Left**: suitable receptive field and suitable dimension. **Mid**: too large receptive field and suitable dimension. **Right**: suitable receptive field and too small dimension.

<img src="examples/recon_FPE_good_alpha.jpg" alt="recon1" style="width:33%;"><img src="examples/recon_FPE_low_alpha.jpg" alt="recon2" style="width:33%;"><img src="examples/recon_FPE_low_dim.jpg" alt="recon2" style="width:33%;">

<u>**Binary Vector Implementation of HDFE:**</u> In addition to the fractional power encoding introduced in the paper, we also implement a binary vector encoding version of HDFE. **It runs faster and yields comparable performance** as the FPE encoding. It has not been optimized for the memory consumption and takes a lot of GPU memory. However, it is not difficult to do that optimization from the methodology perspective. It just requires a lot of engineering, so I haven't done it yet. If you are interested in using this architecture in some real-time applications, and require that implementation. Feel free to contact me at dhyuan@umd.edu.
