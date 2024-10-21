### Order of operations
As the codes needed to be run in a certain order, and some files needed to be manually moved to different folders for the analysis to work, the order of operations is included below.

1. Move the raw videos to the "videos/raw" folder
2. Run shortening_frame_nrs.ipynb
3. Run extract_images_boundaries.ipynb
4. Run extract_images_training.ipynb
5. Move one boundary image corresponding to each camera to the “images/boundary_four” folder - preferably images with the barrier placed
6. Move all boundary images for each video with lids to the “images/with_lids” folder
7. Run the select_boundaries.ipynb codes
8. Move the shortened videos from the “videos/to_analyse/all” to their corresponding folders in the “video/to_analyse” folder ("videos/to_analyse/detour" and "videos/to_analyse/OF_mir" respectively)
9. Run timing.ipynb
10. Train the algorithm on the training images according to the <a href="https://pysource.com/2020/04/02/train-yolo-to-detect-a-custom-object-online-with-free-gpu/">pysource</a> instructions - this includes using Labelimg to mark the trout in the training images, training the model using the code provided by pysource, and potentially extracting more images and retraining if the trained algorithm is not good enough. The training code provided by pysource is not included in the description of the file structure as it is all done via Google collab, as described on the pysource page.
11. Place the files for the trained algorithm in the correct folder ("dnn_model")
12. Run detour.ipynb
13. Run OF_mirror.ipynb
14. Run clear_false_detections.ipynb
15. Run summarising_data.ipynb
