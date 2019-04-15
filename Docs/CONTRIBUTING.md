Contributing to CARLA
=====================

We are more than happy to accept contributions!

How can I contribute?

  * Reporting bugs
  * Feature requests
  * Improving documentation
  * Code contributions

Reporting bugs
--------------

Use our [issue section][issueslink] on GitHub. Please check before that the
issue is not already reported, and make sure you have read our
[Documentation][docslink] and [FAQ][faqlink].

[issueslink]: https://github.com/carla-simulator/carla/issues
[docslink]: http://carla.readthedocs.io
[faqlink]: http://carla.readthedocs.io/en/latest/faq/

Feature requests
----------------

Please check first the list of [feature requests][frlink]. If it is not there
and you think is a feature that might be interesting for users, please submit
your request as a new issue.

[frlink]: https://github.com/carla-simulator/carla/issues?q=is%3Aissue+is%3Aopen+label%3A%22feature+request%22+sort%3Acomments-desc

Improving documentation
-----------------------

If you feel something is missing in the documentation, please don't hesitate to
open an issue to let us know. Even better, if you think you can improve it
yourself, it would be a great contribution to the community!

We build our documentation with [MkDocs](http://www.mkdocs.org/) based on the
Markdown files inside the "Docs" folder. You can either directly modify them on
GitHub or locally in your machine.

Once you are done with your changes, please submit a pull-request.

**TIP:** You can build and serve it locally by running `mkdocs` in the project's
main folder

    $ sudo pip install mkdocs
    $ mkdocs serve

Code contributions
------------------

So you are considering making a code contribution, great! we love to have
contributions from the community.

Before starting hands-on on coding, please check out our
[issue board][wafflelink] to see if we are already working on that, it would
be a pity putting an effort into something just to discover that someone else
was already working on that. In case of doubt or to discuss how to proceed,
please contact one of us (or send an email to carla.simulator@gmail.com).

[wafflelink]: https://waffle.io/carla-simulator/carla

#### Where can I learn more about Unreal Engine?

A basic introduction to C++ programming with UE4 can be found at Unreal's
[C++ Programming Tutorials][ue4tutorials]. Then, if you want to dive into UE4
C++ development there are few paying options online. The
[Unreal C++ Course at Udemy][ue4course] it's pretty complete and there are
usually offers that make it very affordable.

[ue4tutorials]: https://docs.unrealengine.com/latest/INT/Programming/Tutorials/
[ue4course]: https://www.udemy.com/unrealcourse/

#### What should I know before I get started?

Check out the ["CARLA Design"](index.md)<!-- @todo --> document to get an idea
on the different modules that compose CARLA, and chose the most appropriate one
to hold the new feature. We are aware the developers documentation is still
scarce, please ask us in case of doubt, and of course don't hesitate to improve
the current documentation if you feel confident enough.

#### Are there any examples in CARLA to see how Unreal programming works?

You can find an example of how C++ classes work in UE4 in
[`ASceneCaptureToDiskCamera`][capturelink] (and its parent class
`ASceneCaptureCamera`). This class creates an actor that can be dropped into the
scene. In the editor, type _"Scene Capture To Disk"_ in the Modes tab, and drag
and drop the actor into the scene. Now searching for its detail tab you can find
all the `UPROPERTY` members reflected. This shows the basic mechanism to use C++
classes in Unreal Editor.

For a more advanced example on how to extend C++ classes with blueprints, you
can take a look at the _"VehicleSpawner"_ blueprint. It derives from the C++
class `AVehicleSpawnerBase`. The C++ class decides where and when it spawns a
vehicle, then calls the function `SpawnVehicle()`, which is implemented in the
blueprint. The blueprint then decides model and color of the vehicle being
spawned. Note that the blueprint can call back C++ functions, for instance for
getting the random engine. This way there is a back-and-forth communication
between C++ code and blueprints.

[capturelink]: https://github.com/carla-simulator/carla/blob/master/Unreal/CarlaUE4/Plugins/Carla/Source/Carla/Sensor/SceneCaptureToDiskCamera.h

#### Coding standard

Please follow the current [coding standard](coding_standard.md) when submitting
new code.

#### Pull-requests

Once you think your contribution is ready to be added to CARLA, please submit a
pull-request.

Try to be as descriptive as possible when filling the pull-request description.
Adding images and gifs may help people to understand your changes or new
features.

Please note that there are some checks that the new code is required to pass
before we can do the merge. The checks are automatically run by the continuous
integration system, you will see a green tick mark if all the checks succeeded.
If you see a red mark, please correct your code accordingly.

###### Checklist

<!--
  If you modify this list please keep it up-to-date with pull_request_template.md
-->

  - [ ] Your branch is up-to-date with the `master` branch and tested with latest changes
  - [ ] Extended the README / documentation, if necessary
  - [ ] Code compiles correctly
  - [ ] All tests passing with `make check`
