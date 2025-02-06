
In real-time, 

-> instead of classifying each data point, use a model to **detect change points** where the label transitions.

-> define transition rules to avoid unrealistic segments (e.g. short bursts of ACTIVE in the middle of OFF).


**Regression Testing**

-> Set thresholds for acceptable performance

-> Test for edge or corner cases

-> Use statistical tests to ensure observed differences in metrics are not due to random variations dut due to changes in features, model parameters or bugs in preprocessing or post-processing data pipelines, shifts in data distribution.

**Unit Testing**

>> test_model.py

import unittest

import numpy as np

from sklearn.ensemble import RandomForestClassifier

class TestModel(unittest.TestCase):

    def setUp(self):
        self.model = RandomForestClassifier()             #you may load a pre-trained model
        X_train = np.array([[1, 2], [2, 3], [3, 4]])
        y_train = np.array([0, 1, 1])
        self.model.fit(X_train, y_train)
        
        self.test_data = np.array([[1, 2], [3, 4], [2, 2]])
        self.expected_labels = np.array([0, 1, 1])        #Expected output

    def test_model_output_shape(self):
        predictions = self.model.predict(self.test_data)
        self.assertEqual(predictions.shape[0], self.test_data.shape[0])    #matching data shapes

    def test_model_output_correctness(self):
        predictions = self.model.predict(self.test_data)
        np.testing.assert_array_equal(predictions, self.expected_labels)

    def test_model_edge_cases(self):
        edge_case_data = np.array([[0, 0]])           #Example of edge-case input
        prediction = self.model.predict(edge_case_data)
        self.assertIsNotNone(prediction)
        
if __name__ == '__main__':
    
    unittest.main()


>> python -m pytest test_model.py

OR

>> unittest test_model.py
