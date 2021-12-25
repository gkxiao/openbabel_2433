<h2>about openbabel 2433</h2>
<p>This is an example to show how to reproduce the PDBQT tree error resulting in redocking failure repored in <a href="https://github.com/openbabel/openbabel/issues/2433">#2423</a></p>
<h2>Materials</h2>
<ol>
   <li>ligand to be docked: sti.mol2 or sti.sdf</li>
   <li>ligand prepared by openbabel from sti.mol2: sti_ob.pdbqt</li>
   <li>ligand prepared by ADT from sti.mol2: sti_adt.pdbqt</li>
   <li>Vina docking configure file: dock.conf</li>
   <li>protein file prepared for docking: protein.pdbqt</li>
</ol>
<h2>Step to reproduce re-docking faulure</h2>
<p>1. use openbabel pdbqt</p>
<pre>
vina --config dock.conf --ligand sti_ob.pdbqt --out sti_ob_docked.pdbqt 
</pre>
<p>2. use ADT pdbqt</p>
<pre>
vina --config dock.conf --ligand sti_adt.pdbqt --out sti_adt_docked.pdbqt 
</pre>
<p>3. Visualize the docking poses with cognate ligand (reference.sdf) </p>
