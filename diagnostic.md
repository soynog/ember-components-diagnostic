# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    https://cdn.tutsplus.com/net/uploads/2013/11/hierarchy-2.png
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    Each component has a .js file and an .hbs file. The JS file provides functionality for the component, and the HTMLbars file provides a display template.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{my-contact contact=model}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    <ul>
    {{#each contact.phoneNumbers as |num|}}
      <li>{{my-phone num=num}}
    {{/each}}
    </ul>
    ```
