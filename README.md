<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Code Display</title>
    <style>
        .code-container {
            width: 80%;
            margin: 0 auto;
            overflow-x: auto;
            white-space: pre-wrap;
            border: 1px solid #ccc;
            padding: 10px;
            background-color: #f9f9f9;
        }
        .copy-button {
            background-color: #4caf50;
            border: none;
            color: white;
            padding: 10px 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            cursor: pointer;
            border-radius: 8px;
        }
    </style>
</head>
<body>

<div class="code-container" id="codeContainer">
    Solutions:
1)
package quadratic;
import java.util.Scanner;
public class Quadratic 
{
 public static void main(String[] args) 
 {
 double root1, root2,a,b,c,determinant,r;
 Scanner input = new Scanner(System.in);
 System.out.print("Input a: ");
 a = input.nextDouble();
 System.out.print("Input b: ");
 b = input.nextDouble();
 System.out.print("Input c: ");
 c = input.nextDouble();
 determinant = b * b - 4 * a * c;
r=Math.sqrt(determinant);
 
 if (determinant > 0) 
 {
root1 = (-b+r)/(2*a);
 root2 = (-b-r)/(2*a);
 System.out.format("root1 = %.2f and root2 = %.2f\n", root1, root2);
 }
 else if (determinant == 0) 
{
 root1 = root2 = (-b)/(2*a);
 System.out.format("Roots are equal\n");
 System.out.format("root1 = root2 = %.2f\n;", root1);
 }
 else 
 {
 // roots are complex number and distinct
 double real = -b / (2 * a);
 double imaginary = Math.sqrt(-determinant) / (2 * a);
 System.out.format("Roots are imaginary\n");
 System.out.format("root1 = %.2f+%.2fi\n", real, imaginary);
 System.out.format("\nroot2 = %.2f-%.2fi\n", real, imaginary);
 }
 }
}
</div>

<button class="copy-button" onclick="copyCode()">Copy Code</button>

<script>
    function copyCode() {
        var codeContainer = document.getElementById('codeContainer');
        var range = document.createRange();
        range.selectNode(codeContainer);
        window.getSelection().removeAllRanges();
        window.getSelection().addRange(range);
        document.execCommand('copy');
        window.getSelection().removeAllRanges();
        alert('Code copied to clipboard!');
    }
</script>

</body>
</html>
