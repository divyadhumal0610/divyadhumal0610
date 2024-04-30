package subsetSum;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class SubsetSum {

    // Function to find all subsets with given sum using backtracking
    private static void findSubsets(int[] weights, int sum, List<Integer> subset, int index) {
        if (sum == 0) {
            // Print the subset if sum is found
            System.out.println(subset);
            return;
        }

        if (sum < 0 || index >= weights.length) {
            // Backtrack if sum is negative or index exceeds array bounds
            return;
        }

        // Include the current element in the subset
        subset.add(weights[index]);

        // Recur with sum minus current element and move to the next element
        findSubsets(weights, sum - weights[index], subset, index + 1);

        // Exclude the current element from the subset and backtrack
        subset.remove(subset.size() - 1);
        findSubsets(weights, sum, subset, index + 1);
    }

    public static void main(String[] args) {
        int[] weights = {10, 7, 5, 18, 12, 20, 15};
        int sum = 35;
Arrays.sort(weights); // Sort the array to optimize backtracking
        List<Integer> subset = new ArrayList<>();
        findSubsets(weights, sum, subset, 0);
    }
}
