Do This, Not That
===============================================================================

Setting Flags based on a List
-------------------------------------------------------------------------------

Don't do this:

```yaml

# my_flag_list is ['my_flag_1','my_flag_3']

# my_main.yml
- name: Set all Flags
  include_tasks: set_flags.yml
  loop: "{{ my_flag_list }}"
  loop_control:
    loop_var: flag

# set_flags.yml
- name: Set Flag 1
  set_fact:
    my_flag_1: true
  when: flag == "my_flag_1"

- name: Set Flag 2
  set_fact:
    my_flag_2: true
  when: flag == "my_flag_2"

...

```

Do this instead:

```yaml

# my_flag_list is ['my_flag_1','my_flag_3']

# my_main.yml
- name: Set all Flags
  set_fact:
    my_flag_1: "{{ 'my_flag_1' in my_flag_list }}"
    my_flag_2: "{{ 'my_flag_2' in my_flag_list }}"

...

```
