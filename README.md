using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class GunTools : MonoBehaviour
{
    public Transform Object_; //đối tượng Follow
    void Update()
    {
        Vector3 newPos = new Vector3(Object_.position.x, Object_.position.y, 0);
        //lấy tọa độ Object (x,y,z)
        transform.position = Vector3.Slerp(transform.position, newPos, 1);
        //Object hiện tại = vecter3.Slerp(Object hiện tại, Object Follow, tốc độ delay);
    }
}
