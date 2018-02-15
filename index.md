## Welcome to MIX reality group 


### Week 1

Introduction to the course and a quick walkthrough on how vofuria works in unity.
Managed to get a linerendere to reflect a beam once.

### Week 2


using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Laser : MonoBehaviour
{

    private LineRenderer _line;
    private Ray shootRay;
    private RaycastHit shootHit;
    private int _count = 0;
    private bool bounce = true;

    public float _castDistance = 10f;

	// Use this for initialization
	void Start ()
	{
	    _line = gameObject.GetComponent<LineRenderer>();
	    _line.enabled = true;
	    _line.positionCount = 10;
	}
	
	// Update is called once per frame
	void Update ()
	{
        CastLaser();
	}

    void CastLaser()
    {
       

         shootRay = new Ray(transform.position, transform.forward);
        _line.SetPosition(_count++, transform.position);

        while (bounce)
        {
            _count++;
            Debug.Log("Loop");
            if (Physics.Raycast(shootRay, out shootHit, _castDistance))
            {
                Debug.Log("Hit");
                if (shootHit.collider.tag == "Mirror")
                {
                    _line.SetPosition(_count, shootHit.point);
                    shootRay.origin = shootHit.point;
                    shootRay.direction = Vector3.Reflect(shootRay.direction, shootHit.normal);
                    //_line.SetPosition(_count++, shootRay.origin + shootRay.direction * 100f);

                }
                else
                {
                    bounce = false;
                    _line.SetPosition(_count, shootHit.point);
                }

            }
            else
            {

                _line.SetPosition(_count, shootRay.origin + shootRay.direction * _castDistance);
                bounce = false;
            }
        }

        _count = 0;
        bounce = true;




    }
}


