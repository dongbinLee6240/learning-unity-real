# learning-unity-real
Real unity

//PositionScript
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PositionScript:MonoBehaviour

    float moveX, moveY;
    [Header("이동속도 조절")]
[Serializefield][Range(1f, 30f)] float moveSpeed = 20f;

void Update()
{
    //이동(상화자우키:WSAD키 혹은 상화좌우이동기)
    moveX = Input.GetAxis("Horizontal") * moveSpeed * Time.deltaTime;
    moveY = Input.GetAxis("vertical") * moveSpeed * Time.deltaTime;

    transform.position = new Vector2(transform.position.x + movex, transfrom.positionY + moveY);

}
