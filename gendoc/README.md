The intent here is to build a "Generative document" (gendoc)

Unfortunately, what this means is still uncertain...

So, at the moment we are making this up as we go along (whoever we is).
In this particular case, I am essentially making a gendoc for this project (the perhaps poorly named k8s-bot-demo project).

In reaching a more abstract gendoc process, this will seem a little bit overkill, but this is also a motivating process for this project.
The project here, is meant to become an example of a gendoc based project bootstrap.
When mature, there should be something of a mature gendoc attached to the project that exemplifies using gendoc to build a taget project.
There should also be a stab at the more abstract gendoc process itself.  That is another project where the gendoc process is the content of the project.

So in essence, here we are working at two outputs:
1. A specific gendoc documentation system describing how this project is undertaken.
2. Perhaps the same output made as an example for integration into the more abstract gendoc project.

This means output #1 eventually can be refined down and refactored in ways that make it more fit for this k8s-boot-demo project (or whatever we might call it in the future).
Some of the potential categories for the gendoc process will be retained as they relate to this project (history, learnings, etc).
Some of the outputs that might be in this tree to begin with might eventually be pruned out of this project, as ceratin content withing the "categories" may really properly apply to the gendoc project itself.

Let's also keep in mid that part of the gendoc project data might include learning about how specific practices are specified, removed or added as specific to a certain project's needs.
Im a mature form, this means the gendoc might only mention these things, or almost seem "taken for granted" apart from some historical reference or as orientation from the overall gendoc process.

Another attempt (mostly failed) of building gendoc is found here: https://github.com/dcarpent74/CI-Document

Because theis is another nascent attempt, I expect to have a lot more gendoc process documentation here (i.e. we lack a gendoc starting point, so we are figuring that out as we go too).

So, here this is the basic starting point...  We are curerntly building the gendoc for this project with extensive notes and attention to formulating the gendoc process and project at the same time.
Currently, a public github repository is being used, and attempt should be made to simply append edits and changes as thigs go using an as of yet undefined but presumably typical github kind of process.
I would like for most history to be maintained as much as possible and avoid rewriting or squashing history.  Though we do not neceesarily need to keed simple edits to be retained, I would like to retain much of what happens as "learnings"

As we move forward, we should refine bot the documentation process for this project specifcally, but also make sure to capture and refine the gendoc process and documentation as well.
At a point where it seems appropriate, perhaps I will s gendoc repository at which point we can streamline what we are doing here.  Probably still feeding gendoc, but also refining the gendoc for this project to mostly reflect this project.
But for now, both are sort of the same thing.

So how about a quick stab at some conventions:
1. History: rather than modify away stuff, lets try to build a document history area (a sub-directory). Files should have dates as part of the file names: YYYYMMDD-RRR[-YYYYMMDD-RRR]-<text_description_name>.<md|txt|???> The first date should be a source date or optionally a copied out date followed by a source date.  After that a descriptive file name.  Efforts to clarify dates or names, namechanges, etc should be included in the document or in a companion file. Rather than throw away old documents or making major revisions, let's start by collecting any history that we might want to keep.
2. Learning: Often derrived from history, this would be more specifc learnings as we go. gendoc learnings might eventually head off to the gendoc repostiory once there is such a thing (or at least learnings for this project as an exmaple gendoc project).
