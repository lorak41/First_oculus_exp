
FOLLOW THIS FOR THE HANDS TO WORK AND RUN

https://forum.unity.com/threads/quest-update-breaks-input-and-hand-tracking.716807/


The manifest must be in plugins!


https://www.youtube.com/watch?v=sKQOlqNe_WY

https://circuitstream.com/oculus-quest-unity-setup/



https://forum.unity.com/threads/how-to-make-anim-out-of-obj-sequence.479423/

    public Mesh activeFrame;
    MeshFilter mf;
    void Start () {
        mf = GetComponent<MeshFilter>();
    }
   
    void Update () {
        mf.mesh = activeFrame;
    }

Then I simply animate activeFrame variable to change model.
This is horrible solution. If i have aroud 80 models animated like this my framefate drop to half but for now it is enough. I'll have time for tweaking later.

https://wirewhiz.com/vr-button-in-unity/


I found out that if you check "Parent Held Transform" on both AvatarGrabberLeft/Right, the object stops jittering while grabbed. Unfortunately this also produced a strange misalignment of the hands while moving them around.

https://www.reddit.com/r/Unity3D/comments/c0vlmf/oculus_quest_jittery_movement_objects/?st=jzk7clvh&sh=8a88f4d7

another fix