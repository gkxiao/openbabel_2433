<h2>Materials</h2>
<ol>
   <li>ligand prepared by openbabel: sti_ob.pdbqt</li>
   <li>ligand prepared by rdkit: sti_adt.pdbqt</li>
   <li>Vina docking configure file: dock.conf</li>
   <li>protein file prepared for docking: protein.pdbqt</li>
</ol>
<h2>Step to reproduce docking faulure</h2>
<p>1. use openbabel pdbqt</p>
<pre>
vina --config dock.conf --ligand sti_ob.pdbqt --out sti_ob_docked.pdbqt 
</pre>
<p>2. use ADT pdbqt</p>
<pre>
vina --config dock.conf --ligand sti_adt.pdbqt --out sti_adt_docked.pdbqt 
</pre>
<p>3. Visualize the docking poses with cognate ligand (reference.sdf) </p>
