# INTRODUCTION
- Terraform's language is its primary user interface. Configuration files you write in Terraform language tell Terraform what plugins to install, what infrastructure to create, and what data to fetch. Terraform language also lets you define dependencies between resources and create multiple similar resources from a single configuration block.
- The main purpose of the Terraform language is declaring resources, which represent infrastructure objects. All other language features exist only to make the definition of resources more flexible and convenient.
- A Terraform configuration is a complete document in the Terraform language that tells Terraform how to manage a given collection of infrastructure. A configuration can consist of multiple files and directories.
  ```
  <BLOCK TYPE> "<BLOCK LABEL>" "<BLOCK LABEL>" {
            # Block body
            <IDENTIFIER> = <EXPRESSION> # Argument
        }
  ```
  - Blocks : are containers for other content and usually represent the configuration of some kind of object, like a resource. Blocks have a block type, can have zero or more labels, and have a body that contains any number of arguments and nested blocks. Most of Terraform's features are controlled by top-level blocks in a configuration file.
  - Arguments : assign a value to a name. They appear within blocks.
  - Expressions : represent a value, either literally or by referencing and combining other values. They appear as values for arguments, or within other expressions
- The Terraform language is declarative, describing an intended goal rather than the steps to reach that goal. The ordering of blocks and the files they are organized into are generally not significant; Terraform only considers implicit and explicit relationships between resources when determining an order of operations
