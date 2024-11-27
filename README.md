using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class NPC : MonoBehaviour
{

    //NPC health
 public int health = 10;
    //NPC level
 public int level = 1;
    //NPC Speed
 public float speed = 1.2f;
    // Start is called before the first frame update
    void Start()
    {
        health = health + level;
        Debug.Log("lives: " + health);
    }

    // Update is called once per frame
    void Update()
    {
       Vector3 newPosition = this.transform.position;

        newPosition.z =  newPosition.z + speed * Time.deltaTime;


     this.transform.position = newPosition;
    }
}
