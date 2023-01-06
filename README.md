# prodigy-labels
Importing prodi.gy dataset in jupyter notebook, reading labels and exporting list of words per label

This code connects to a SQLite database and retrieve a dataset with the name "new_dataset", then perform some analysis on the data. It first creates an empty list called label_names and iterates over the examples in the dataset. For each example, it checks whether the answer field is equal to "accept". If it is, it iterates over the spans field of the example and tries to extract the label field for each span. If it is successful, it appends the label to the label_names list.

Next, the code creates a set from the label_names list and converts the set back into a list. This will remove any duplicate elements from the label_names list. The code then iterates over the resulting list and prints each item.

The second block of code creates a defaultdict called label_stats and then iterates over the examples in the dataset again. For each example, it checks whether the answer field is equal to "accept", and if it is, it iterates over the spans field of the example. It tries to extract the label field and the corresponding slice of the text from the text field of the example, and if the label is "OUTPUT", it appends the text to the label_stats defaultdict. Finally, the code prints the list stored under the key "OUTPUT" in the label_stats defaultdict.
