# CSS Exercises

These exercises consist of a series of CSS-related tasks intended to complement the HTML and CSS content on The Odin Project (TOP). They should only be completed when instructed during the course of the curriculum.

When doing these exercises, please use all documentation and resources you need to accomplish them. You are _not_ intended to have any of this stuff memorized at this point. Check the docs, use Google, and do what you need to do (besides checking the solutions) to get them done.

> [!IMPORTANT]
> We encourage you to practice your git skills by committing your changes and pushing them to your own fork.  However, please **DO NOT** open a Pull Request to have your solutions merged into this repo or to show your solution.  If we were to merge your changes the exercises would no longer be available as intended for new learners, and opening a PR only causes additional work for us, as we have to close it without merging.

## Contributing

If you have suggestions to improve an exercise, ideas for a new exercise, or notice an issue with an exercise, please feel free to open an issue after thoroughly reading our [contributing guide](https://github.com/TheOdinProject/.github/blob/main/CONTRIBUTING.md).

## How To Use These Exercises

1. Fork and clone this repository. To learn how to fork a repository, see the GitHub documentation on how to [fork a repo](https://docs.github.com/en/get-started/quickstart/fork-a-repo).
    - Copies of repositories on your machine are called clones. If you need help cloning to your local environment, you can learn how from the GitHub documentation on [cloning a repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository).
1. Go to an exercise directory and open the HTML file in a web browser. You can open the file directly or use something like VSCode's Live Server extension.
1. For each exercise, read the README thoroughly before starting any work.
    - Each README has a "Self Check" list. Use this to ensure you haven't missed any important details in your implementation.
1. Make your edits in the `index.html` and/or the `style.css` files in order to make the output in your browser look like the Desired Outcome image(s).
    - Depending on the instructions of the exercise, you may only need to make edits in one of these files.
1. Once you successfully finish an exercise, check TOP's solution to compare it with yours.
    - You should not be checking the solution for an exercise until you finish it!
    - If your solution differs wildly from TOP's solution (and still passes the exercise's requirements), that's completely fine. Do feel free to ask about it in our Discord if there are parts you do not understand.

> [!IMPORTANT]
> Do not submit your solutions to this repo, as any PRs that do so will be closed without merging.

## Some Hints
- The official solutions put all changes at the _end_ of the CSS file, which may duplicate some selectors (e.g. there might be a `body {}` in the given CSS and another `body {}` in the solution). When you are working on an exercise, it is best practice to add your CSS to existing selectors instead of duplicating them at the end of the file. We're sacrificing this best practice in our official solutions to make it extra clear to you what things we changed to solve the exercise.
- Unless listed in the self-check section, do not worry about getting the exact pixel value for things like margin, padding and font size. These exercises are intended to test your knowledge of CSS, not your ability to guess that a screenshot is using `font: sans-serif bold 16px` or that the margin is _exactly_ `42px`.
- You may need to add some elements to your HTML to get things into the right spot. (For the first few exercises, we make it explicit when this needs to happen.)
- You may need to add more selectors to your CSS file. The first few exercises have almost everything already done for you, but as you progress, you'll find that you need to add more and more selectors to get the correct result.


# Anotaciones buenas practicas del lado del front end --  With Benjamin Destefanis (Full-Stack Developer)

## Alta prioridad

1. Minimazar el numero de frames (Use iframes solo si no tiene ninguna otra posibilidad técnica. Intenta evitar los iframes tanto como puedas. Los Iframes no solo son malos para el rendimiento, sino también para la accesibilidad y la usabilidad. Los iframes tampoco están indexados por los motores de búsqueda.)
2. Minimizar CSS - Remover Comentarios -- Espacios en blanco -- (Cuando se minifican los archivos CSS, el contenido se carga más rápido y se envían menos datos al cliente. Es importante minimizar siempre los archivos CSS en producción. Es beneficioso para el usuario, ya que es para cualquier empresa que quiera reducir los costos de ancho de banda y reducir el uso de recursos.
Use herramientas para minimizar sus archivos automáticamente antes o durante su compilación o implementación.)
3. Los archivos CSS deben no bloquearse para evitar que el DOM tome tiempo para cargarse. -- (Los archivos CSS pueden bloquear la carga de la página y retrasar la representación de su página. Usando preload en realidad, puede cargar los archivos CSS antes de que el navegador comience a mostrar el contenido de la página.
Necesitas agregar el rel atributo con el valor de precarga y añadir as="style" en el <link> elemento.)
4. CSS Critico en Linea -- (El CSS crítico (o “sobre el fold”) recopila todo el CSS utilizado para representar la parte visible de la página. Está incrustado antes de su llamada CSS principal y entre <style></style> en una sola línea (minificada si es posible).

La incorporación de CSS crítico ayuda a acelerar la representación de las páginas web reduciendo el número de solicitudes al servidor.

Genera el CSS crítico con herramientas online o usando un plugin como el que desarrolló Addy Osmani.)