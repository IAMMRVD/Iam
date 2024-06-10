<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Java Code Snippets</title>
<style>
    pre {
        background-color: #f4f4f4;
        padding: 10px;
        border-radius: 5px;
        overflow-x: auto;
    }
</style>
</head>
<body>

<h1>Java Code Snippets</h1>

<pre id="code1">
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
</pre>

<pre id="code2">
public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }
}
</pre>

<pre id="code3">
public class Fibonacci {
    public static void main(String[] args) {
        int n = 10, t1 = 0, t2 = 1;
        System.out.print("First " + n + " terms: ");

        for (int i = 1; i <= n; ++i) {
            System.out.print(t1 + " + ");

            int sum = t1 + t2;
            t1 = t2;
            t2 = sum;
        }
    }
}
</pre>

<pre id="code4">
public class Factorial {
    public static void main(String[] args) {
        int n = 5, factorial = 1;

        for (int i = 1; i <= n; ++i) {
            factorial *= i;
        }

        System.out.println("Factorial of " + n + " = " + factorial);
    }
}
</pre>

<pre id="code5">
public class PrimeNumber {
    public static void main(String[] args) {
        int num = 29;
        boolean isPrime = true;

        for (int i = 2; i <= num / 2; ++i) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }

        if (isPrime)
            System.out.println(num + " is a prime number.");
        else
            System.out.println(num + " is not a prime number.");
    }
}
</pre>

<pre id="code6">
public class ReverseString {
    public static void main(String[] args) {
        String str = "Hello, World!";
        StringBuilder reversed = new StringBuilder();

        for (int i = str.length() - 1; i >= 0; --i) {
            reversed.append(str.charAt(i));
        }

        System.out.println("Reversed string: " + reversed);
    }
}
</pre>

<pre id="code7">
public class ArraySum {
    public static void main(String[] args) {
        int[] numbers = {1, 2, 3, 4, 5};
        int sum = 0;

        for (int number : numbers) {
            sum += number;
        }

        System.out.println("Sum: " + sum);
    }
}
</pre>

<pre id="code8">
public class Palindrome {
    public static void main(String[] args) {
        String str = "madam";
        String reversed = "";

        for (int i = str.length() - 1; i >= 0; --i) {
            reversed += str.charAt(i);
        }

        if (str.equals(reversed))
            System.out.println(str + " is a palindrome.");
        else
            System.out.println(str + " is not a palindrome.");
    }
}
</pre>

<button onclick="copyCode(1)">Copy Code 1</button>
<button onclick="copyCode(2)">Copy Code 2</button>
<button onclick="copyCode(3)">Copy Code 3</button>
<button onclick="copyCode(4)">Copy Code 4</button>
<button onclick="copyCode(5)">Copy Code 5</button>
<button onclick="copyCode(6)">Copy Code 6</button>
<button onclick="copyCode(7)">Copy Code 7</button>
<button onclick="copyCode(8)">Copy Code 8</button>

<script>
function copyCode(id) {
    var code = document.getElementById('code' + id);
    var range = document.createRange();
    range.selectNode(code);
    window.getSelection().removeAllRanges();
    window.getSelection().addRange(range);
    document.execCommand("copy");
    window.getSelection().removeAllRanges();
    alert("Code " + id + " copied to clipboard!");
}
</script>

</body>
</html>
