
<!DOCTYPE html>
<html>
<head>
    
</head>
<body>

<h1>Distance Calculations in Python</h1>

<p>This repository contains Python code snippets for calculating various types of distances used in machine learning and data analysis. The code examples provided cover Euclidean, Manhattan, Hamming, Cosine similarity, Jaccard similarity, and a general distance calculation.</p>

<h2>1. Euclidean Distance Calculation</h2>

<p>To calculate the Euclidean distance between two points <code>\(\mathbf{x}\)</code> and <code>\(\mathbf{y}\)</code>:</p>

<pre><code>import numpy as np

# Define the points
x = np.array([3, 4])
y = np.array([4, 3])

# Calculate Euclidean distance
euclidean_distance = np.linalg.norm(x - y)
print(f'Euclidean Distance: {euclidean_distance}')
</code></pre>

<h2>2. Manhattan Distance Calculation</h2>

<p>To calculate the Manhattan distance between two blocks (vectors):</p>

<pre><code># Define the blocks
block1 = np.array([5, 2, -3, 4])
block2 = np.array([1, 6, -7, 8])

# Calculate Manhattan distance
manhattan_distance = np.sum(np.abs(block1 - block2))
print(f'Manhattan Distance: {manhattan_distance}')
</code></pre>

<h2>3. Hamming Distance Calculation</h2>

<p>To calculate the Hamming distance between two binary strings:</p>

<pre><code>from scipy.spatial import distance
import numpy as np

# Define binary strings
x1 = np.array([0, 0, 0, 1, 0, 1, 1, 0, 1, 1, 1, 0, 0, 0, 1])
x2 = np.array([0, 1, 0, 1, 0, 1, 0, 1, 0, 1, 0, 1, 0, 1, 0])

# Calculate Hamming distance
hamming_distance = distance.hamming(x1, x2) * len(x1)  # Multiply by length to get the count of differing bits
print(f'Hamming Distance: {hamming_distance}')
</code></pre>

<h2>4. Cosine Similarity and Distance Calculation</h2>

<p>To calculate the Cosine similarity and distance between two vectors:</p>

<pre><code>from sklearn.metrics.pairwise import cosine_similarity
import numpy as np

# Define the vectors
a = np.array([2, 3]).reshape(1, -1)
b = np.array([2, 2]).reshape(1, -1)

# Calculate Cosine similarity
cos_sim = cosine_similarity(a, b)[0][0]
# Calculate Cosine distance
cos_dist = 1 - cos_sim

print(f'Cosine Similarity: {cos_sim}')
print(f'Cosine Distance: {cos_dist}')
</code></pre>

<h2>5. Jaccard Distance Calculation</h2>

<p>To calculate the Jaccard distance between two sets:</p>

<pre><code>from sklearn.metrics import jaccard_score
import numpy as np

# Define the sets
X = np.array([1, 1, 1, 0])  # (1 for presence, 0 for absence)
Y = np.array([0, 1, 1, 1])

# Calculate Jaccard similarity
jac_sim = jaccard_score(X, Y)
# Calculate Jaccard distance
jac_dist = 1 - jac_sim

print(f'Jaccard Similarity: {jac_sim}')
print(f'Jaccard Distance: {jac_dist}')
</code></pre>

<h2>6. General Distance Example Calculation</h2>

<p>To calculate a general distance between two vectors, you can use various distance metrics. Here's an example with Euclidean distance:</p>

<pre><code>import numpy as np

# Define the vectors
a = np.array([1, 2, 3, 4, 5])
b = np.array([1, 2, 3, 4, 6])

# Calculate Euclidean distance
general_distance = np.linalg.norm(a - b)
print(f'General Distance (Euclidean): {general_distance}')
</code></pre>

<h2>Running the Code</h2>

<p>You can run these snippets in a Python environment such as Google Colab or any other Jupyter notebook. Each snippet is designed to be self-contained and can be executed independently.</p>

<p>Feel free to modify the code snippets to suit your specific use cases or datasets.</p>

</body>
</html>
