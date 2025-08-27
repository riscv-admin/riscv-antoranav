# Global Navigation for RISC-V Docs

This repo contains the global navigation files used by the RISC-V documentation site.

- Holds the main navbar (`nav.adoc`) and site landing page (`index.adoc`).  
- Included as a content source in the Antora playbook.  
- Defines the shared navigation across all docs components.

**Note:** This repo must be a Git repository so Antora can use it as a content source.

If you need to update the navigation, edit the files in `modules/ROOT/`.

---

## About `include::isa::nav.adoc[]`

In the navigation files, you may see statements like:

```
include::isa::nav.adoc[]
```

This tells Antora to include the navigation from the component named `isa`.

### What to change:


- Replace `isa` with the **component name** of the content source whose navigation you want to include.  
- The component name is defined in each component’s `antora.yml` file under the `name:` key.

For example, if you want to include the nav from the component `component-a`, you would write:

```
include::component-a::nav.adoc[]
```

Make sure that the referenced component is included as a content source in the Antora playbook (located in another repo.)

---

If you have questions about component names or updating navigation, check the respective `antora.yml` files or reach out to the docs team.
