It is worth noting that you can combine multiple selectors and combinators together. For example:

/* selects any <span> that is inside a <p>, which is inside an <article>  */

article p span {
}

/* selects any <p> that comes directly after a <ul>, which comes directly after an <h1>  */

h1 + ul + p {
}