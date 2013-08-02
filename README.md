BufTimer
========

Time your editing duration

This small plugin uses Vims `reltime` feature, to measure how long you spend editing your files.

This means, it defines a couple of autocommands to start and stop a timer per buffer. You can see the timing statistics by using `:BufTimer` for the current buffer or `:BufTimerReport` for all buffers (what all buffers mean, depends on the configuration variable `g:btrOpt` variable).

This plugin is based on Bill McCarthys [BufTimer][1] plugin which itself is based on a [discussion][2] on the [vim mailinglist][3], but has been further rewritten.

[1]: https://groups.google.com/d/msg/vim_use/Hd1p6iIx9KY/AZ6cXBP9uL4J
[2]: https://groups.google.com/d/msg/vim_use/QgPspne7hRU/NjkFsfgPFjMJ
[3]: https://groups.google.com/group/vim_use


Configuration
-------------

There are only some configuration items, to further refine the behaviour of this plugin.

* `g:btrOpt`
This variable determines, which buffers it will consider when outputting the `:BufTimerReport` statistics. Values:
  0. *0*  consider all existing buffers,
  1. *1* consider only listed buffers,
  2. *2* consider only loaded buffers.
  (default value: 0)
* `g:buftimer_map`
This Variable can be set to a keys combination to trigger the output of the `:BufTimer` report. To specify a key mapping, simply put into your .vimrc:
    :let g:buftimer_map = "<leader>bt"
(default value: not set)
* `g:buftimer_report_map`
This Variable can be set to a keys combination to trigger the output of the `:BufTimer` report. To specify a key mapping, simply put into your .vimrc:
    :let g:buftimer_report_map = "<leader>br"
(default value: not set)


License & Copyright
-------

Based on work by Bill McCarthy. Further developed by Christian Brabandt. 
The Vim License applies. See `:h license`
