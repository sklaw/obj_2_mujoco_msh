## Usage
`
python convert_obj_to_mujoco_msh.py [your_file.obj]
`

If the script runs without errors, a file of `msh` will be generated at the same directory.

## Reference from Mujoco.org

>  The binary MSH file starts with 4 integers specifying the number of vertex positions (nvertex), vertex normals (nnormal), vertex texture coordinates (ntexcoord), and vertex indices making up the faces (nface), followed by the numeric data. nvertex must be at least 4. nnormal and ntexcoord can be zero (in which case the corresponding data is not defined) or equal to nvertex. nface can also be zero, in which case faces are constructed automatically from the convex hull of the vertex positions. The file size in bytes must be exactly: 16 + 12*(nvertex + nnormal + nface) + 8*ntexcoord. The contents of the file must be as follows:

    (int32)   nvertex
    (int32)   nnormal
    (int32)   ntexcoord
    (int32)   nface
    (float)   vertex_positions[3*nvertex]
    (float)   vertex_normals[3*nnormal]
    (float)   vertex_texcoords[2*ntexcoord]
    (int32)   face_vertex_indices[3*nface]
