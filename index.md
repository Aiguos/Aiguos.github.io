## Welcome to MIX reality group 


### Week 1

Introduction to the course and a quick walkthrough on how vofuria works in unity.
Managed to get a linerendere to reflect a beam once.

### Week 2

void DrawLaserBeam()
	{
		_line.SetPosition(0,transform.position);
		shootRay.origin = transform.position;
		shootRay.direction = transform.forward;

		if(Physics.Raycast(shootRay,out shootHit,1000f))
		{			
			if(shootHit.collider.tag == "Mirror")
			{
				_line.SetPosition(1,shootHit.point);
				shootRay.origin = shootHit.point;
				shootRay.direction = Vector3.Reflect(shootRay.direction,shootHit.normal); 
				_line.SetPosition(2,shootRay.origin + shootRay.direction * 100f);

			}

		}
		else
		{

			_line.SetPosition(1,shootRay.origin + shootRay.direction * 1000f);	
		}


	}
