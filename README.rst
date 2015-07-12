=======
overrun
=======

run container over the root.

overview
========

``overrun`` setup overlayfs on the root filesystem and run nspawn container in it.

usage
=====

.. code:: console

  # overrun [nspawn options]

example
=======

.. code:: console

  # overrun
  Spawning container lbA32APzCA on /tmp/tmp.lbA32APzCA/root.
  Press ^] three times within 1s to kill container.
  lbA32APzCA# echo hello > /hello.txt
  lbA32APzCA# exit
  Container lbA32APzCA exited successfully.
  # cat /hello.txt
  cat: /hello.txt: No such file or directory
  # cat /tmp/tmp.lbA32APzCA/upper/hello.txt
  hello
