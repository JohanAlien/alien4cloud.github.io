---
layout: post
exclude_from_search: true
title:  get_input
root: ../../../
categories: DOCUMENTATION-1.2.0
parent: [devops, tosca_concepts, tosca_ref_definitions, tosca_ref_types_function_definition]
node_name: tosca_ref_get_input
weight: 100
---

The **get_input** function is used to retrieve the values of properties declared within the inputs section of a TOSCA Service Template.

## Grammar

{% highlight yaml %}
get_input: <input_property_name>
{% endhighlight %}

## Example

{% highlight yaml %}
inputs:
  cpus:
    type: integer
  node_templates:
    my_server:
      type: tosca.nodes.Compute
      properties:
        num_cpus: { get_input: cpus }
{% endhighlight %}