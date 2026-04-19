# Backpake

// 1. Reverse a String
const reverseString = (s: string): string => {
    let result = "";
    for (let i = s.length - 1; i >= 0; i--) {
        result += s[i];
    }
    return result;
};

// 2. FizzBuzz
const fizzBuzz = (n: number): void => {
    for (let i = 1; i <= n; i++) {
        if (i % 3 === 0 && i % 5 === 0) {
            console.log("FizzBuzz");
        } else if (i % 3 === 0) {
            console.log("Fizz");
        } else if (i % 5 === 0) {
            console.log("Buzz");
        } else {
            console.log(i);
        }
    }
};

// 3. Find the Largest Number
const findLargest = (nums: number[]): number => {
    let max = nums[0];
    for (let i = 1; i < nums.length; i++) {
        if (nums[i] > max) {
            max = nums[i];
        }
    }
    return max;
};

// 4. Check for Palindrome
const isPalindrome = (s: string): boolean => {
    let clean = "";
    
    // clean string (remove non-alphanumeric & lowercase)
    for (let i = 0; i < s.length; i++) {
        let ch = s[i].toLowerCase();
        if ((ch >= 'a' && ch <= 'z') || (ch >= '0' && ch <= '9')) {
            clean += ch;
        }
    }

    // check palindrome
    let left = 0;
    let right = clean.length - 1;

    while (left < right) {
        if (clean[left] !== clean[right]) {
            return false;
        }
        left++;
        right--;
    }

    return true;
};

// 5. Sum of Array Elements
const sumArray = (nums: number[]): number => {
    let sum = 0;
    for (let i = 0; i < nums.length; i++) {
        sum += nums[i];
    }
    return sum;
};


const countVowels = (s: string): number => {
    let count = 0;
    const vowels = "aeiouAEIOU";

    for (let i = 0; i < s.length; i++) {
        if (vowels.includes(s[i])) {
            count++;
        }
    }

    return count;
};

// 7. Factorial Calculation
const factorial = (n: number): number => {
    if (n === 0) return 1;

    let result = 1;
    for (let i = 1; i <= n; i++) {
        result *= i;
    }

    return result;
};

// 8. Even Numbers Only
const getEvens = (nums: number[]): number[] => {
    let result: number[] = [];

    for (let i = 0; i < nums.length; i++) {
        if (nums[i] % 2 === 0) {
            result.push(nums[i]);
        }
    }

    return result;
};

// 9. Fibonacci Sequence
const fibonacci = (n: number): number[] => {
    if (n === 1) return [0];

    let result: number[] = [0, 1];

    for (let i = 2; i < n; i++) {
        let next = result[i - 1] + result[i - 2];
        result.push(next);
    }

    return result;
};

// 10. Find the Minimum
const findMinimum = (nums: number[]): number => {
    let min = nums[0];

    for (let i = 1; i < nums.length; i++) {
        if (nums[i] < min) {
            min = nums[i];
        }
    }

    return min;
};
