Download Link: https://assignmentchef.com/product/solved-cs6476-problem-set
<br>
Unless otherwise stated, there is a single best answer for each multiple choice question.

[p1] <em>Human Vision</em>. The human eye is analogous to cameras in many ways. Which of the following statements about the human are true? <em>Choose <strong>all</strong> that are correct</em> (a) Rods have little to do with color perception in bright scenes.

<ul>

 <li>Cones are active only during low light situations.</li>

 <li>Rods are highest density in the Fovea (center of our visual field).</li>

 <li>Colors are perceived in bright scenes based on the relative color sensitivities of Rods versusCones.</li>

 <li>People typically have 3 types of cones sensitive to 3 different ranges of wavelengths (color blind persons can be an exception).</li>

</ul>

[p2] <em>Cameras</em>. A typical camera sensor (as you’d find in a cell phone) measures which attributes of the photons coming from a scene? <em>Choose <strong>all</strong> that are correct </em>(a) The number of “bounces” a photon took off various scene surfaces

<ul>

 <li>The position that a photon hit the sensor (equivalent to the angle that a photon passed through the “pinhole”)</li>

 <li>The amount of time that a photon existed</li>

 <li>The rate of photons hitting the sensor (flux)</li>

 <li>The distance a photon traveled</li>

 <li>The wavelength of a photon hitting the sensor</li>

</ul>

[p3] <em>Image Formation</em>. Which of the following properties of 3d lines are preserved during image formation under perspective projection with the pinhole camera model?

<ul>

 <li>relative lengths of lines</li>

 <li>angles between lines</li>

 <li>parallelism between lines</li>

 <li>straightness of lines</li>

</ul>

Image formation with a pinhole camera model is described mathematically as  p<sub>image</sub> = K [ R | T] p<sub>world</sub>  where p<sub>image</sub> is an image coordinate and p<sub>world</sub> is a world coordinate.

[p4] <em>Image Formation</em>. What is the matrix K?

<ul>

 <li>This “intrinsic” matrix converts 3d camera coordinates to image coordinates.</li>

 <li>This matrix integrates the exposure over time accounting for world and camera motion.</li>

 <li>This matrix accounts for distortions caused by the camera lens.</li>

 <li>This “extrinsic” matrix rotates and translates the world coordinate system to align with the camera coordinate system.</li>

</ul>

[p5] <em>Image Formation</em>. What is the matrix [R | T]?

<ul>

 <li>This “intrinsic” matrix converts 3d camera coordinates to image coordinates.</li>

 <li>This matrix integrates the exposure over time accounting for world and camera motion.</li>

 <li>This matrix accounts for distortions caused by the camera lens.</li>

 <li>This “extrinsic” matrix rotates and translates the 3D world coordinate system to align with the3D camera coordinate system.</li>

</ul>

[p6] <em>Image Formation</em>. How many degrees of freedom does the matrix [R | T] have?

[p7] <em>Image Formation</em>. In lecture we mentioned that K can be modeled with different numbers of free parameters — in fact the book mentions 8, 7, 5, 3, and 1 parameter versions. The 1 parameter version, which models only the <em>most important</em> parameter, is of this form:

What is this “?” parameter and what is its physical meaning?

[p8] <em>Frequency Domain</em>. Convolution in the spatial domain is equivalent to element-wise multiplication in the Fourier domain. Why might this be useful?

<ul>

 <li>Since element-wise multiplication is very fast, it may be faster to convert the image and filter to the frequency domain, multiply them, and convert back to the image domain rather than performing the convolution in the spatial domain as we did in project 1.</li>

 <li>Many common filters only exist in the Fourier domain and have no spatial domain representation, so we have to work in the Fourier domain for those filters.</li>

 <li>When filtering in the spatial domain you can have boundary artifacts where the filter doesn’t fit into the image near the edges of the image. In the Fourier domain there are no boundary artifacts because it magically hallucinates content outside the image boundaries. (d) Working in the Fourier domain is more numerically accurate.</li>

</ul>

[p9] <em>Filtering</em>. If we convolve an image A with filter B to produce result C (A * B = C), can we invert the convolution (i.e. recover A from B and C)?

<ul>

 <li>No, never. Convolution always removes information (e.g. blurs away high frequencies) and there’s no way to recover that information even approximately.</li>

 <li>Kind of. Filters typically attenuate but do not completely remove particular frequencies from A(equivalently, the fourier transform of a filter is mostly non-zero amplitudes). These attenuated frequencies can be approximately recovered by division of C by B in the Fourier domain. As particular frequencies of B approach zero amplitude this approximation becomes worse. (c) Yes, sometimes. For some trivial cases (e.g. B is identity or a shift filter) then A is easy to recover. For all other filters you cannot even approximate A given B and C.</li>

</ul>

(d) Yes, always. Convolution is multiplication in the Fourier domain, and multiplication is inverted by division. Thus any convolution is invertible.

[p10] <em>Features</em>. Why do the majority of local features, such as the SIFT feature you implemented, characterize the spatial <em>gradients</em> of intensities in an image patch rather than the raw pixel intensities?

<ul>

 <li>gradients are invariant to image rotation.</li>

 <li>gradients are invariant to image scaling.</li>

 <li>gradients are invariant to constant brightness shifts.(d) gradients don’t have noise but pixel intensities do.</li>

</ul>

[p11] <em>Model Fitting and Outlier Rejection</em>. We want to use a Hough transform to find arbitrary triangles in an image. Triangles can be parametrized by the location of the 3 corners for a total of 6 degrees of freedom. How much memory is needed to run this Hough transform?

<ul>

 <li>6 ints to store the image coordinates of the best model currently discovered.</li>

 <li>K ^ 6 ints, where K is the number of discrete bins for each spatial dimension.(c) 6 ^ K ints, where K is the number of discrete bins for each spatial dimension. (d) 6 * K ints, where K is the number of discrete bins for each spatial dimension.</li>

</ul>

[p12] <em>Model Fitting and Outlier Rejection</em>. RANSAC is an algorithm to robustly find the best parameters for a model. To find the best line parameters given a large set of points, briefly outline the steps of the RANSAC algorithm

[p13] <em>Model Fitting and Outlier Rejection</em>. Which of the following is a potential advantage of RANSAC over the Hough transform?

<ul>

 <li>With RANSAC it is easier to simultaneously fit multiple independent models (e.g. 3 different affine transformations) which fit different parts of the data well.</li>

 <li>With RANSAC there is no need to discretize the model’s parameter space and store an accumulator array over this parameter space.</li>

 <li>The stopping conditions of RANSAC are more clearly defined than the Hough transform.</li>

</ul>

[p14] <em>Stereo</em>. Which of the following statements correctly describes the relationship between disparity and depth?

<ul>

 <li>Depth and disparity are independent.</li>

 <li>Depth is proportional to disparity.</li>

 <li>Depth is proportional to the square root of disparity.(d) Depth is inversely proportional to disparity.</li>

</ul>

[p15] <em>Stereo. </em>Which of the following is a property of the Fundamental Matrix F? x and x’ are homogeneous pixel coordinates, from cameras at location o and o’ respectively, represented as 3 x 1 vectors.

<ul>

 <li>x<sup>T</sup> * F * x’ = 1 only when points x and x’ correspond to the same 3d point.</li>

 <li>x<sup>T</sup> * F * x’ = 0 implies that points x and x’ could be projections of the same 3d point.</li>

 <li>x<sup>T</sup> * F = x’ for points x and x’ at the same depth.</li>

 <li>F = x’ * x<sup>T</sup> if x’ and x are the projections of the other cameras (o and o’).</li>

</ul>

[p16] <em>Tracking and Optical flow</em>. In the context of tracking and optical flow, explain the “aperture problem” and how it is mitigated?

<ul>

 <li>The “aperture problem” is an illusion specific to human perception of motion. The illusion does not need to be mitigated by tracking algorithms.</li>

 <li>Tracking and optical flow is ambiguous with simple intensity features. Using color and texturedescriptors mitigates the aperture problem.</li>

 <li>Without knowing the parameters of the camera aperture, tracking and optical flow are fundamentally ambiguous. Camera calibration eliminates the ambiguity.</li>

 <li>In small image regions, true motions can be ambiguous if the image content is flat or onedimensional. Reasoning about larger windows or only tracking corners reduces the ambiguity.</li>

</ul>

[p17] <em>Tracking and Optical flow</em>. Which of the following is <strong>NOT</strong> an assumption of the classical Lucas-Kanade optical flow discussed in class:

<ul>

 <li>Parallel motion: points only move parallel to the imaging plane in 3d</li>

 <li>Brightness constancy: projection of the same point looks the same in every frame</li>

 <li>Spatial coherence: points move like their neighbors</li>

 <li>Small motion: points do not move very far</li>

</ul>