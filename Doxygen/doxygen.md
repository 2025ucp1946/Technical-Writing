# Doxygen

## What is Doxygen?

Doxygen is a documentation generator. It reads specially formatted comments in source code and creates documentation from them. It is commonly used with languages such as C, C++, and Java.

## Why use Doxygen?

- Explains what functions, classes, and files do.
- Creates documentation from source-code comments.
- Helps other programmers understand a project.
- Can generate HTML and LaTeX documentation.

## Example in C

```c
/**
 * @file main.c
 * @brief A simple addition program.
 */

/**
 * @brief Adds two integers.
 * @param a First number.
 * @param b Second number.
 * @return Sum of a and b.
 */
int add(int a, int b)
{
    return a + b;
}
```

## Common Doxygen commands

- `@file`: describes a source file.
- `@brief`: gives a short description.
- `@param`: describes a function parameter.
- `@return`: describes the returned value.
- `@author`: gives the author's name.
- `@see`: refers to related documentation.

## Basic workflow

1. Add Doxygen-style comments to the source code.
2. Create a configuration file using `doxygen -g`.
3. Open the generated `Doxyfile`.
4. Set options such as `INPUT`, `OUTPUT_DIRECTORY`, and `GENERATE_HTML`.
5. Run `doxygen Doxyfile`.
6. Open the generated HTML documentation, usually in the output directory's `html` folder.

## Example commands

```bash
doxygen -g
doxygen Doxyfile
```

## What I learned

I learned that Doxygen can generate readable project documentation from comments written inside source code.


## Example program with output

Save this complete example as \`main.c\`:

\`\`\`c
/**
 * @file main.c
 * @brief Program to add two numbers.
 */

/**
 * @brief Adds two integers.
 * @param a First number.
 * @param b Second number.
 * @return Sum of the numbers.
 */
int add(int a, int b)
{
    return a + b;
}

int main(void)
{
    int result = add(10, 5);
    return 0;
}
\`\`\`

This example demonstrates documentation comments. The function returns 15 when called with 10 and 5. It does not print the result because there is no \`printf\` statement.

## Generate the documentation

Run these commands in the folder containing \`main.c\`:

\`\`\`bash
doxygen -g
\`\`\`

Expected terminal message (wording can vary by Doxygen version):

\`\`\`text
Configuration file 'Doxyfile' created.
\`\`\`

In \`Doxyfile\`, set or check these options:

\`\`\`text
INPUT = main.c
EXTRACT_ALL = YES
GENERATE_HTML = YES
GENERATE_LATEX = NO
\`\`\`

Then run:

\`\`\`bash
doxygen Doxyfile
\`\`\`

Expected result:

- Doxygen reads the comments in \`main.c\`.
- It creates an HTML documentation folder (often named \`html\`).
- Open \`html/index.html\` in a web browser.
- The generated page contains the file description and the \`add\` function documentation, including its parameters and return value.

The exact terminal messages and generated folder names depend on the Doxyfile settings and Doxygen version.
